# FFMpeg Online
This repository maintains a list of FFMpeg commands for different situations.

Maintained by <a href="https://hotpot.ai?s=ffmpeg-online">Hotpot.ai</a>. Hotpot.ai offers AI tools and drag-n-drop software for graphic design and media creation.

We plan to launch an online FFmpeg service. Please join the beta list if interested.

Please make a pull request to edit this list.

# Requests
1. Command for turning HTMl5 animations into WebP videos?

# Commands
Please list scenarios and commands here. Where possible, please cite and credit the command creators.

**Convert videos to 720p web-playable videos**
* Creator: https://github.com/nicbou/
* https://github.com/nicbou/homeserver/blob/22c0a160f9df5f4c34cc7a0dc322d5461a73a28b/videoprocessing/src/jobs.py#L97

**Create hover previews like on modern streaming sites**
* Creator: https://github.com/nicbou/
* https://github.com/nicbou/timeline/blob/9d9340930ed0213dffdd884bef17f65c73e86ffc/backend/source/timeline/file_utils.py#L31

**Convert videos to GIFs**
* Creator:
* https://engineering.giphy.com/how-to-make-gifs-with-ffmpeg/
* `ffmpeg -ss 61.0 -t 2.5 -i StickAround.mp4 -filter_complex "[0:v] fps=12,scale=480:-1,split [a][b];[a] palettegen [p];[b][p] paletteuse" SmallerStickAround.gif`
