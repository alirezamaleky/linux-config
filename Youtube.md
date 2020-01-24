# Youtube

## Install

```bash
apt install -y youtube-dl
```

## Playlist

```bash
youtube-dl --ignore-errors --proxy socks5://127.0.0.1:9050 -o '%(playlist)s/%(title)s.%(ext)s' <playlist_link>
```

## Audio

```bash
youtube-dl --ignore-errors --proxy socks5://127.0.0.1:9050 --extract-audio --audio-format mp3 --audio-quality 128K -o '%(playlist)s/%(title)s.%(ext)s' <playlist_link>
```
