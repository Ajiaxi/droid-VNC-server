Fork of droid-VNC-server that uses openstf's minicap shared library for screen capture, with some additional features.
WIP - Currently only works as a VNC viewer

# Quickbuild

```
brew install android-ndk
git submodule update --init
ndk-build
...
adb push libs/* /data/local/tmp/androidvncserver
adb shell /data/local/tmp/androidvncserver/androidvncserver
```

Tah dah!

# Original docs

See [OLD-README.md](OLD-README.md]
