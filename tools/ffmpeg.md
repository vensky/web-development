# [Easy video converting for the web](https://mefody.dev/chunks/ffmpeg-alias/)

ffmpeg -i input.mov -map_metadata -1 -an -c:v libx264 \
-crf 24 -preset veryslow -profile:v main -pix_fmt yuv420p \
-movflags +faststart -vf "scale=trunc(iw/2)*2:trunc(ih/2)*2" \
output.h264.mp4
