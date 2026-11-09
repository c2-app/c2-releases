# C2 下载与安装 · Téléchargement · Download

**最新版 / Dernière version / Latest:** <https://github.com/c2-app/c2-releases/releases/latest>

已经装好的 C2 会自己提示更新，一般不用来这里下载。第一次使用需要管理员给的**邀请码**。

| 系统 | 下载哪个文件 |
|---|---|
| Windows 10 / 11 | `C2-<版本>-setup.exe` |
| Mac（Apple 芯片：M1 / M2 / M3 / M4） | `C2-<版本>-mac.zip` |
| Linux（Ubuntu 22.04 及以上等） | `C2-<版本>-x86_64.AppImage`（推荐）或 `C2-<版本>-amd64.deb` |

---

## Windows

1. 下载 `C2-<版本>-setup.exe`，双击运行。
2. 如果出现蓝色窗口「Windows 已保护你的电脑」：点 **「更多信息」→「仍要运行」**。
3. 装好后从开始菜单打开 **C2**，粘贴邀请码登录。

## Mac

1. 下载 `C2-<版本>-mac.zip`，双击解压，把 **C2** 拖进「**应用程序**」文件夹。
2. 第一次打开时，Mac 可能提示「**C2 已损坏，无法打开**」或「**无法验证开发者**」。这是因为 C2 没有在苹果商店上架，不是真的损坏。打开「**终端**」（启动台 → 其他 → 终端），粘贴下面这行，按回车：

   ```bash
   xattr -dr com.apple.quarantine /Applications/C2.app
   ```

3. 再双击打开 C2，粘贴邀请码登录。
4. 要让 Claude 帮你看屏幕，需要在「**系统设置 → 隐私与安全性 → 屏幕与系统录音**」里打开 C2，然后重新打开 C2。

> 请从「应用程序」文件夹打开 C2，不要直接在「下载」文件夹里运行，否则自动更新会失败。

## Linux

**AppImage（推荐，能自动更新）**

```bash
chmod +x C2-*-x86_64.AppImage
./C2-*-x86_64.AppImage
```

如果提示缺少 FUSE：Ubuntu 22.04 运行 `sudo apt install libfuse2`，Ubuntu 24.04 运行 `sudo apt install libfuse2t64`。

**.deb（Ubuntu / Debian，需手动更新）**

```bash
sudo apt install ./C2-*-amd64.deb
```

---

## Français

- **Windows** : lancez `C2-<version>-setup.exe`. Si Windows affiche « Windows a protégé votre ordinateur », cliquez sur **Informations complémentaires → Exécuter quand même**.
- **Mac** : décompressez le zip, glissez **C2** dans **Applications**. Si macOS dit que l'app est « endommagée » ou que le développeur ne peut être vérifié, ouvrez le **Terminal** et collez :
  `xattr -dr com.apple.quarantine /Applications/C2.app` — puis ouvrez C2.
- **Linux** : `chmod +x C2-*-x86_64.AppImage` puis lancez-le (installez `libfuse2` si besoin), ou `sudo apt install ./C2-*-amd64.deb`.
- La première connexion demande un **code d'invitation** de l'administrateur. Les versions installées se mettent à jour d'elles-mêmes.

## English

- **Windows**: run `C2-<version>-setup.exe`. If SmartScreen says "Windows protected your PC", click **More info → Run anyway**.
- **Mac**: unzip, drag **C2** into **Applications**. If macOS says the app is "damaged" or the developer cannot be verified, open **Terminal** and paste
  `xattr -dr com.apple.quarantine /Applications/C2.app`, then open C2.
- **Linux**: `chmod +x C2-*-x86_64.AppImage` and run it (install `libfuse2` if asked), or `sudo apt install ./C2-*-amd64.deb`.
- Signing in the first time needs an **invite code** from the administrator. Installed apps update themselves.
