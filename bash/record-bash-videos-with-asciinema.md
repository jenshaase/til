# Record bash videos with Asciinema

(Asciinema)[https://asciinema.org/] is a tool to record and share terminal sessions.

## Install

```
sudo apt-get install asciinema

cat <<EOT >> $HOME/.config/asciinema/config
[api]
; Protect me from publishing to asciinema
url = https://asciinema.example.com

[record]
; Protect privacy by setting prompt to >
command = PS1="> " /bin/bash --norc
EOT
```

## Start recording

```
asciinema rec my-cast.json
```

## Convert to GIF using asciicast2gif

[asciicast2gif](https://github.com/asciinema/asciicast2gif) is a tool for generating GIF animations from asciicast files recorded by asciinema.

```
docker run --rm -v $PWD:/data asciinema/asciicast2gif [options and arguments...]

# Example (See https://github.com/asciinema/asciicast2gif#usage)
docker run --rm -v $PWD:/data asciinema/asciicast2gif -s 2 -t solarized-dark my-cast.json my-cast.gif
```

# Convert GIF to MP4

```
ffmpeg -i animated.gif -movflags faststart -pix_fmt yuv420p -vf "scale=trunc(iw/2)*2:trunc(ih/2)*2" video.mp4
```
