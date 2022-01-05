<h1 align="center">NOTFLIX FOR MAC</h1>
<p align="center">notflix-mac is a command terminal tool that search magnet links and stream it with webtorrent</p>

### Introduction
It is like a Netflix but in reality it is a scraper that take magnetic torrent links and easily stream the chosen movie.

I stole the idea from [notflix](https://github.com/Bugswriter/notflix)

### How does this work?

This is a C shell script. It scrapes from 1337x and gets the magnet link.
After this it uses [webtorrent](https://webtorrent.io/) to stream the video from the magnet link.
For scraping, the script uses simple gnu utils like grep, sed, awk, paste, cut.

## Usage
Open ZSH terminal and enter the name of the script followed by keywords of the movie that you want to see.
```sh
notflix-mac the title of the movie
```
To swim through many page (if there are other page) select 0, otherwis you can chose the movie entering the desired number.

## Dependencies
# webtorrent
To install with brew:
```sh
brew install webtorrent-cli
```

# mpv
Get it on the [official site: https://mpv.io/installation/](https://mpv.io/installation/)
then you need to add mpv path to the PATH variable in ZSH.

Open configuration file of ZSH writing
```sh
nano ~/.zshrc
```
Concatenate "/Applications/mpv.app/Contents/MacOS" between the colons ":" of the PATH variable. In my case PATH variable becomes:
```sh
export PATH=/opt/homebrew/bin:/Applications/mpv.app/Contents/MacOS:$PATH
```
So a PATH variable is being set somewhere.

## Installation on Mac (maybe work on linux too)

```sh
$ sudo curl -sL "https://github.com/EmilioSchi/notflix-mac/master/notflix-mac" -o /usr/local/bin/notflix-mac
$ sudo chmod +x /usr/local/bin/notflix-mac
```

## Uninstall
```sh
rm -f /usr/local/bin/notflix-mac
```
