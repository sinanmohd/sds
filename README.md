# sds - sinan's (or simple) dmenu scripts (formerly xorg only)
[dmenu](https://tools.suckless.org/dmenu/) is a fast and lightweight dynamic menu for X written by the
[suckless](https://suckless.org/) community. this is my collection of posix scripts for dmenu like
programs. these scipts were initially made for dmenu with xorg in mind, now
they work on both xorg and wayland using dmenu and wmenu respectively. these
scripts might use font awesome, make sure you've installed them for the best
experience. you can find more info about them below.

## dbook
dbook is a bookmark manager, it can bookmark directories, files, text, links,
anything, by default dbook will try to represent the data best way possoble
ie open links using the browser, coppy text to clipboard, if it's a video
open using a video player, etc. use -i or -s to add an entry or directly
modify the config file located at ~/.config/dbook/dbook.conf. dbook can
also copy bookmarks and type them.

## dpass
dpass is the dmenu wrapper for the standard unix password manager,
run dpass -h from a terminal to see what it's capable of.
reasons to use dpass over passmenu
* dpass is posix compliant.
* dpass keeps the tree structure of pass.

## damb - dmenu ambience
listen to ambient music while working on somthing fun. audio files should be
stored at ~/.local/share/damb/. damb also has a config file located
at ~/.conf/damb/links, where you can provide direct links to media sources or
links to youtube-dl supported sites, it should be in the
format, name = link, you can also play links from your clipboard using
the stream option. mix together varous ambient sounds and stream with damb

## pirowatch
pirowatch is a dmenu wrapper for [web torrent](https://webtorrent.io/), provide magnet or torrent files
as command line argument or input from dmenu and consoom the media using [mpv](https://mpv.io/).
if you pass "-s" as the first argument it'll skip index selection to speed up
the launching

## 1337x
scraper for 1337x.to, has an optional dependency on pirowatch. if you pass "-o"
as the first argument it'll print the scraped magnet link to stdout otherwise
it will pass the magnet link to pirowatch

## yts
scraper for yts.mx, has an optional dependency on pirowatch. if you pass "-o"
as the first argument it'll print the scraped torrent link to stdout otherwise
it will pass the link to pirowatch

## menu_run
this scripts does the same job as the dmenu_run script, they why use it?
dmenu_run depends on stest, they will not be available if you're not
running xorg and don't have dmenu installed. menu_run only uses built in sh
commands but if the cache is not prepared dmenu_run will run about
1.16 +- 0.04 faster than the mentioned script, if it is then menu_run
will run 2.54 +- 0.26 faster than dmenu_run, which will be the most likely
situation . though the scale of the gains are very small the main goal
of the script is to get rid of dependence on stest and dmenu

## vpn
dmenu wrapper for wireguard, has an optional dependency on wip. you can pass
wireguard config name as the first argument otherwise it will use the default
value which is "wg0"

## wip - what is my ip
wip queries host's ipv4 address using opendns and displays the ip details using
the geoip database

## daskpass
this can be used as a password prompt. to use it with sudo set SUDO_ASKPASS

## dunicode
script to copy and type unicode characters
