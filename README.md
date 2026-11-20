# PPgiao123 游戏公开信息与隐私政策仓库 (`Game_Policy`)

本公开仓库用于托管 **PPgiao123** 旗下所有游戏的开发者官网 MVP、游戏简介页及隐私政策静态页面（通过 GitHub Pages 对外提供 HTTPS 访问，不依赖任何外部脚本或字体）。

> **安全红线**：**严禁向本公开仓库上传任何 `.keystore`、`.jks`、密码、私钥、签名文件或闭源游戏源码。**

## 目录结构与线上访问地址

```text
Game_Policy/
├── index.html                   # Play Console 开发者官网（MVP）
└── ArrowGO/
    ├── index.html               # ArrowGO 游戏简介与支持页
    └── privacy/
        └── index.html           # ArrowGO 五语隐私政策（v1.8.2 无广告版）
```

在 GitHub 仓库开启 Pages 后（注意路径区分大小写）：
- **开发者官网（MVP）**：`https://ppgiao123.github.io/Game_Policy/`
- **ArrowGO 简介页**：`https://ppgiao123.github.io/Game_Policy/ArrowGO/`
- **ArrowGO 隐私政策 URL**：`https://ppgiao123.github.io/Game_Policy/ArrowGO/privacy/`

## 开启 GitHub Pages 步骤

1. 确保仓库 `PPgiao123/Game_Policy` 为 **Public（公开）**。
2. 打开仓库页面 **Settings -> Pages**（`https://github.com/PPgiao123/Game_Policy/settings/pages`）。
3. **Build and deployment / Source** 选择 **`Deploy from a branch`**。
4. **Branch** 选择 **`main`** 和 **`/ (root)`**，点击 **Save**。
5. 等待 1~2 分钟部署完成后，用浏览器**无痕模式**打开上述链接确认能正常访问，再分别填入 Google Play Console：
   - **Store settings -> Website**：`https://ppgiao123.github.io/Game_Policy/`
   - **App content -> Privacy policy**：`https://ppgiao123.github.io/Game_Policy/ArrowGO/privacy/`

## 未来扩展其他游戏与 AdMob `app-ads.txt` 说明

- **新增游戏**：在仓库根目录新建对应游戏目录（例如 `ConquerGo/privacy/index.html`、`PlayWord/privacy/index.html`），并在根目录 `index.html` 增加游戏卡片链接即可。
- **未来接入正式 AdMob 时**：Google AdMob 要求 `app-ads.txt` 必须位于开发者网站域名根目录（即 `https://ppgiao123.github.io/app-ads.txt`，不能带 `/Game_Policy/` 子路径）。届时只需：
  - **方式 A**：将本仓库重命名为 `ppgiao123.github.io`（站内均使用相对路径，重命名后无需改页面代码，根目录即变为 `https://ppgiao123.github.io/`，可同时更新 Play Console 的官网与隐私链接）；或
  - **方式 B**：额外新建一个只放 `app-ads.txt` 的公开仓库 `ppgiao123.github.io`，或绑定自定义域名。
