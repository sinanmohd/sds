# sds - sinan's dmenu scripts (formerly xorg only)
[dmenu](https://tools.suckless.org/dmenu/) is a fast and lightweight dynamic menu for X written by the
[suckless](https://suckless.org/) community. this is my collection of posix scripts for dmenu like
programs. these scipts were initially made for dmenu with xorg in mind, now
they work on both xorg and wayland using dmenu and wmenu respectively. these
scripts might use [nerd fonts](https://www.nerdfonts.com/), make sure you've installed them for the best
experience. you can find more info about them below.

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

## vpn
dmenu wrapper for wireguard, has an optional dependency on wip. you can pass
wireguard config name as the first argument otherwise it will use the default
value which is "wg0"

## wip - what is my ip
wip queries host's ipv4 address using opendns and displays the ip details using
the geoip database
