Fork of droid-VNC-server that uses openstf's minicap shared library for screen capture, with some additional features.
WIP - Currently only works as a VNC viewer

# Build

Modify [jni/Application.mk](jni/Application.mk) for the architecture you want. See the [minicap 
docs](https://github.com/openstf/minicap/blob/master/jni/Application.mk) for reference.

Actually build it:

```
brew install android-ndk
git submodule update --init
ndk-build  # takes a while...
adb push rotate.apk /data/local/tmp
adb push libs/<architecture> /data/local/tmp/vnc
adb shell "LD_LIBRARY_PATH=/data/local/tmp /data/local/tmp/vnc/androidvncserver"
```

Tah dah!

# rotate.apk

You can build this yourself from https://github.com/openstf/RotationWatcher.apk

# Original docs

See [OLD-README.md](OLD-README.md)
