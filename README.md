Fork of droid-VNC-server that uses openstf's minicap shared library for screen capture, with some additional features.
WIP - Currently only works as a VNC viewer

# Quickbuild

Modify the architecture you want in [jni/Application.mk](jni/Application.mk). See the [minicap 
docs](https://github.com/openstf/minicap/blob/master/jni/Application.mk) for reference.

Actually build it:

```
brew install android-ndk
git submodule update --init
ndk-build  # takes a while...
adb push libs/* /data/local/tmp/androidvncserver
adb shell /data/local/tmp/androidvncserver/androidvncserver
```

Tah dah!

# Original docs

See [OLD-README.md](OLD-README.md]
