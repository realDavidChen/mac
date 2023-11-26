## 解决 Mac 长按连续输入的问题。😊

您可以通过以下步骤实现 Mac 长按连续输入的功能：

- 打开终端应用程序，输入以下命令¹²⁴⁵：

```bash
defaults write -g ApplePressAndHoldEnabled -bool false
```

- 输入您的管理员密码（如果需要）。
- 注销或重启您的 Mac，使设置生效。

这样，您就可以在文本区域中按住某些键盘键，键的字符将开始重复。例如，只要按住 Delete 键，就会继续移除文本。您也可以设定必须按住按键多久后按键才开始重复，并设置重复开始后的按键重复速率³。

如果您想恢复默认设置，您可以在终端中输入以下命令：

```bash
defaults write -g ApplePressAndHoldEnabled -bool true
```

然后再次注销或重启您的 Mac。
