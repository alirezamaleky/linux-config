# Ffmpeg

## Install

```bash
apt install -y ffmpeg x265 x264
```

## Convert to audio

```bash
ffmpeg -i <input> -vn -ar 44100 -ac 2 -ab 128k -f mp3 <output>
```

## Compress video

```bash
ffmpeg -i <input> -c:v libx265 -crf 28 -c:a aac -b:a 128k <output>
```

## Fast convert

```bash
ffmpeg -i <input> -vcodec copy -acodec copy <output>
```
