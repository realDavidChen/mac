## scrcpy 手机与mac共享屏幕.md

# On macOS

## Install

Scrcpy is available in [Homebrew]:

```bash
brew install scrcpy
```

[Homebrew]: https://brew.sh/

You need `adb`, accessible from your `PATH`. If you don't have it yet:

```bash
brew install android-platform-tools
```

Alternatively, Scrcpy is also available in [MacPorts], which sets up `adb` for you:

```bash
sudo port install scrcpy
```

[MacPorts]: https://www.macports.org/

_See [build.md](build.md) to build and install the app manually._


## Run

_Make sure that your device meets the [prerequisites](/README.md#prerequisites)._

Once installed, run from a terminal:

```bash
scrcpy
```

or with arguments (here to disable audio and record to `file.mkv`):

```bash
scrcpy --no-audio --record=file.mkv
```

Documentation for command line arguments is available:
 - `man scrcpy`
 - `scrcpy --help`
 - on [github](/README.md)

## 关于用scrcpy与手机无线连接的方法：
```
手机在usb调试模式下，连接电脑，打开命令行工具，输入 adb devices, 记下手机的ip地址，因为现在的路由器都是用动态ip的，所以我们要继续下一个操作 adb tcpip 5555 把动态ip设置为静态
这个时候，可以拔掉手机连接线 用 adb connect 192.***.***.*:5555 如果连接成功，会返回 connected to 192.***.***.*:5555
最后，输入 scrcpy 你就可以在无线的情况下，共享屏幕了



```
