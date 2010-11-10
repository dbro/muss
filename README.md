muss
====

The no-fuss, no-muss way to play music from the command line

Introduction
------------

Ready to move beyond slow and complicated music collection
management software?

Do you find yourself spending too much time clicking, scrolling,
dragging, dropping just to hear your favorite slow-jam?

muss is a simple and very fast command line tool to play music.
Its goal is to minimize time spent browsing through lists of
artists/songs/albums/tracks.

What kind of people would use muss?
* often know what music they want to hear
* appreciate the ability to browse sometimes
* typically have easy access to a command line
* seek to minimize music player overhead (time, memory, cpu, etc)
* do not care about flashy displays of album art, lyrics, ratings
* do not want to learn yet another quirky graphical interface, even
  if it is only ncurses
* do not want to spend time creating lots of different playlists

Usage
-----
muss works entirely from the command line (no mouse). It builds a 
playlist for the mpc client based on keywords entered at the command 
line; or through an interactive instant-search of your music library.

muss searches for matches in the mpd database of file names and 
playlist names. Then it automatically starts playing the songs. It
can play internet radio streams when they are included in a playlist.

There are no configuration settings for muss beyond what is already 
set up with mpc and mpd. To install, simply copy the muss executable 
file into your search path (eg /usr/local/bin/).

Quicksearch mode examples:
    muss rolling stones
    muss roll sto
    muss guns roses not heaven
    muss playlist my_faves

Interactive mode:
    muss

Requirements
------------
* mpc, mpd
* sed, grep
* filenames and directory names should be useful.
  If you have a lot of files named "track01.mp3", they probably
  wont be matched as individual songs. If you put them in well-named
  folders like "/Beatles/Abbey Road/track01.mp3" then you can
  at least find them by artist or album name.
* dmenu patched to support xmms-style pattern matching (-xs),
  filtermode (-f) to support multiple items in the result,
  xft fonts (-fa) (the xft requirement will be removed later)
  Note these patches are available here:
  http://github.com/dbro/dmenu-patches
* xft Inconsolata font (the xft requirement will be removed later)
  http://www.levien.com/type/myfonts/inconsolata.html

To Do
-----
* remove xft requirement
* add help/usage message

Thank you
---------
The primary inspiration for a simple command-line approach came from
[plait](http://stephenjungels.com/jungels.net/projects/plait/) which
showed the convenience a partial-text search. It has some additional
features not found in muss (support for multiple players, shoutcast
stream searching).

After using plait for a while, I sometimes missed the ability to
scan and browse for music that I had forgotten. But browsing seemed
to be too slow -- the emphasis on sorting and browsing is what makes
those graphical music programs so cumbersome. Eventually I saw the
excellent browsing speed and simplicity demonstrated by the program
launcher based on [dmenu](http://tools.suckless.org/dmenu/) included
with many text-centric linux distributions.

muss is an attempt to combine the best of both modes, search and browse.
The name can be thought of as an abbreviation of "music search". It is
also an idiom heard in TV commercials to imply a messy hassle ("no fuss!
no muss!") which is what the over-complicated music players can be. Lastly,
also a German word that translates to English as "must", which appeals
to the idea that the computer should be responding to commands from 
people, and not the other way around.

Dan Brown, 2010
