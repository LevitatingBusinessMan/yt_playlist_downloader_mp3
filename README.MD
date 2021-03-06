# YT_MP3
This [NodeJS](https://nodejs.org) command allows you to download youtube playlists in MP3 format complete with ID3 tags.

#### Installation
`npm install yt_mp3_downloader -g`

#### Usage
```
Usage: bin [options] <ID>

Options:
  -v, --version           output the version number
  -s, --streams <amount>  amount of download streams (default: 15)
  -o, --output <dir>      Specify folder to place playlist in
  -a, --album <name>      Specify album name. Options: none, playlist, channel
  --no-image              disable ablum covers (thumbnails)
  --no-ID3                disable ID3 tags
  --no-m3u                don't create m3u file
  --no-overwrite          disable overwriting existing files
  -h, --help              output usage information
```
The ID supplied might either be a direct playlist ID or a link to a playlist.

The streams option defaults to 15, this can be extremely CPU heavy as each download stream has to be converted to mp3.

#### ID3 tags
```
An ID3 tag is a data container within an MP3 audio file stored in a prescribed format. This data commonly contains the Artist name, Song title, Year and Genre of the current audio file.
```
yt_mp3 can automatically set the artist, song title and album cover for each song. This is done by assuming the format of `artist - title` is followed for each video's title. Otherwise the video title will be used as song title, and the artist tag is set to "unknown". On default the first video's thumbnail is set as album cover. The playlists name is saved as album name. ID3 tags can be disabled by using the `--no-ID3` option.