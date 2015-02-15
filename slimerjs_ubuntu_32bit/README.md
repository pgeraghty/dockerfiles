# SlimerJS on Ubuntu 14.04 i386
### SlimerJS 0.9.3

### Notes
Latest version at time of writing (0.9.5) dies on first run with error:
```
/usr/bin/slimerjs: line 173:   101 Segmentation fault      (core dumped) "$SLIMERJSLAUNCHER" -app "$SLIMERDIR/application.ini" $PROFILE -no-remote "$@" 2> /dev/null
```
Subsequent runs yield normal results.

## Usage
```
docker run --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/root/.Xauthority --net=host pgeraghty/slimerjs_ubuntu_32bit --version
```
```
docker run -i -t --rm --entrypoint=bash -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/root/.Xauthority --net=host pgeraghty/slimerjs_ubuntu_32bit
```
