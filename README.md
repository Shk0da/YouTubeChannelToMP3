# YouTubeChannelToMP3
Few steps for download and convert channel from YouTube to mp3

## 1. Install Python

> sudo apt-get install python3.2

> sudo apt install python3-pip

> pip3 install --user youtube-dl

> sudo ln -s /usr/bin/python3 /usr/local/bin/python

## 2. Download all videos from YoutTube Channel

> youtube-dl -f best -ciw -o "%(title)s.%(ext)s" -v **CHANNEL_URI**

## 3. Install ffmpeg & Create outputs directory

> sudo apt install ffmpeg

> mkdir outputs

## 3. Convert all videos in mp3

> for f in *.mp4; do ffmpeg -i "$f" -c:a libmp3lame "outputs/${f%.mp4}.mp3"; done

## It's done.
