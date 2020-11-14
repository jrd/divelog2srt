# divelog2srt

Create depth subtitles from you dive computer regarding media recording under water

# Requirements

`ffmpeg`/`ffprobe` and `python3` should be installed on your computer.

Your videos should need to be recognized by ffprobe (which means quite all formats).

The dive log format supported right now is one from [SubSurface](https://subsurface-divelog.org). 

# Windows

zip bundle is available in the release github pages. You can also use the `create-windows-zip-bundle` from a Linux box.

# Usage

```text
usage: divelog2srt [-h] [-t DIFF_IN_SECS] [-d DIVE_NB] [-f] [-m]
                   logbook media_directory

Extract deep information from dives to .srt files for medias (videos/photos)
mask video embeded subtitles files could also be generated

positional arguments:
  logbook
  media_directory

optional arguments:
  -h, --help            show this help message and exit
  -t DIFF_IN_SECS, --time DIFF_IN_SECS
                        Number of seconds to add to dive log samples (could be
                        negative)
  -d DIVE_NB, --dive DIVE_NB
                        Only selected dive number
  -f, --feet            Output in feet instead of meters
  -m, --mask            Also create a subtitle mask video per subtitle
```

`.srt` files follow the [SubRip format](https://en.wikipedia.org/wiki/SubRip).

`video_deepmask.mp4` files can be use as a mask on a [non-linear video editing software](https://en.wikipedia.org/wiki/Non-linear_editing) (background is black and subtitles are white).

