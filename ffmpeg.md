# FFMPEG Cheat Sheet


## Convert from MOV to MP4

```shell
ffmpeg -i input.mov -acodec copy -vcodec copy output.mp4
```

## Roate Video by 90 Degree

```shell
ffmpeg -i input.mp4 -vf "transpose=1" output.mp4
```

For the transpose parameter you can pass:

0 = 90 Counter Clockwise and Vertical Flip (default)
1 = 90 Clockwise
2 = 90 Counter Clockwise
3 = 90 Clockwise and Vertical Flip

## Get Resolution of Video

```shell
$(ffprobe -v error -of flat=s=_ -select_streams v:0 -show_entries stream=height,width input.mp4)
size=${streams_stream_0_width}x${streams_stream_0_height}
echo $size
```

## Scale Video

```shell
ffmpeg -i input.mp4 -vf scale=1920:1080 output.mp4
```

## Crop Video

```shell
ffmpeg -i input.mp4 -filter:v "crop=1080:1920:0:0" output.mp4
```

[Go Back](README.md)
