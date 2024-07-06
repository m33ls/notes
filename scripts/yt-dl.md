# yd-dlp scripts

download playlist as mp3 and save to subfolder in ~/music
```
yt-dlp -o "~/music/%(playlist)s/%(titles.%(ext)s" -x --audio-format mp3
```

download playlist to youtube folder
```
yt-dlp -o "youtube/%(playlist)s/%(title)s.%(ext)s"
```
