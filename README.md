UPDATE
--------------------
Apparently, vk.com does not allow to acces audio via API anymore, so this project is obsolete.

vk-to-spotify
=============

Part 0: Install libs
--------------------

First, install libspotify (you need <b>premium spotify account</b> for that, sorry).  
see https://pyspotify.mopidy.com/en/latest/installation/

Then, install dependencies:
  pip install -r requirements.txt

If pyspotify pip install fails, try to install it like this:

    pip install --pre pyspotify

Part 1: dump vk.com tracks
--------------------------

You need to set `VK_ID`, `VK_EMAIL`, `VK_PASS` in `vk_save.py`.
Then (with virtualenv activated):
  
    python vk_save.py
  
After this, you will have songs.json in the same folder.

Part 2: upload tracks to spotify
--------------------------------
Download libspotify binary key, details https://pyspotify.mopidy.com/en/latest/quickstart/#application-keys.

Set `SPOTIFY_LOGIN`, `SPOTIFY_PASS`, `PLAYLIST_URI` in `spotify_update.py`, where `PLAYLIST_URI` is the Spotify URI of your playlist where songs will appear.
Then (with virtualenv activated):
   
    python spotify_update.py
  
