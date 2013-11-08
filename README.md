Mopify
======

A mopidy webclient based on the Spotify webbased interface. If you use Mopidy in combination with local music this client probably won't work.
This client uses the Spotify API to speed up searching and artist/ablum lookup.

Features
--------
- Search and album/artist lookup using the Spotify API
- Album cover caching
- Logic user interface based on the [Spotfiy web player](http://play.spotify.com)

Quick install
-------------

Drop the Mopify folder in a folder on your Mopidy-system. Then change the [settings of Mopidy](http://docs.mopidy.com/en/latest/config/) to make it work. 

Example (assuming the webclient is in /opt/webclient):
```code
[http]
enabled = true
hostname = ::
port = 6680
static_dir = /opt/webclient
```


Usage
-----

After you installed the Mopidy client you can use a modern browser (like Firefox or Chrome) to open it. The first time you start the client it will ask for a [two-letter language code](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). We need this code to provide better search results, since we are using the Spotify API.


Security
--------

(Note from Mopidy:) Note that the HTTP frontend does not feature any form of user authentication or authorization. Anyone able to access the web server can use the full core API of Mopidy. Thus, you probably only want to make the web server available from your local network or place it behind a web proxy which takes care or user authentication. You have been warned.

Known bugs/TODO
---------------

- Better Cache system to improve load time on the Artist and Album pages.
- Right click to add tracks to the current tracklist
- Create/Modify playlists
- Add keyboard support
- Not all music returned by the Spotify API is playable. This has something the do with countries and shit like that.
