# FFMpeg Online
This repository maintains a list of FFMpeg commands for different situations.

Maintained by <a href="https://hotpot.ai?s=ffmpeg-online">Hotpot.ai</a>. Hotpot.ai offers AI tools and drag-n-drop software for graphic design and media creation.

We plan to launch an online GUI-based FFmpeg service. Please join the beta list if interested.

# How To Contribute?
We welcome any and all contributors who can help demystify the almighty FFmpeg.

Please make a pull request to edit this list.


# Requests
1. Command for turning HTML5 animations into WebP videos?

# Scenarios & Commands
Where possible, please credit and link to the command creators.

**Convert videos to 720p web-playable videos**
* Creator: https://github.com/nicbou/
* https://github.com/nicbou/homeserver/blob/22c0a160f9df5f4c34cc7a0dc322d5461a73a28b/videoprocessing/src/jobs.py#L97

**Create hover previews like on modern streaming sites**
* Creator: https://github.com/nicbou/
* https://github.com/nicbou/timeline/blob/9d9340930ed0213dffdd884bef17f65c73e86ffc/backend/source/timeline/file_utils.py#L31

**Convert videos to GIFs**
* Creator: https://engineering.giphy.com/
* https://engineering.giphy.com/how-to-make-gifs-with-ffmpeg/
* `ffmpeg -ss 61.0 -t 2.5 -i StickAround.mp4 -filter_complex "[0:v] fps=12,scale=480:-1,split [a][b];[a] palettegen [p];[b][p] paletteuse" SmallerStickAround.gif`

**Compress videos**
* Creator: https://github.com/benwinding
* https://github.com/benwinding/dotfiles/blob/master/bin/ffcompress
* `ffmpeg -i INPUT.mp4 -vcodec libx265 -crf 28 OUTPUT.mp4`

**Extract audio from a video**
* Creator: https://www.commandlinefu.com/
* https://www.commandlinefu.com/commands/matching/ffmpeg/ZmZtcGVn/sort-by-votes
* `ffmpeg -i video.avi -f mp3 audio.mp3`

**Convert all JPEG images to MP4**
* Creator: https://www.commandlinefu.com/
* https://www.commandlinefu.com/commands/view/2005/play-high-res-video-files-on-a-slow-processor
* `cat *.jpg | ffmpeg -f image2pipe -r 1 -vcodec mjpeg -i - -vcodec libx264 out.mp4`

**Create single-image video with audio**
* Creator: https://www.commandlinefu.com/
* https://www.commandlinefu.com/commands/view/12216/creating-a-single-image-video-with-audio-via-ffmpeg
* `ffmpeg -loop 1 -i image.png -i sound.mp3 -shortest video.mp4`
