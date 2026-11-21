# PPgiao123 游戏公开信息与隐私政策仓库 (`ppgiao123.github.io`)

本公开仓库用于托管 **PPgiao123** 旗下所有游戏的开发者官网 MVP、游戏简介页及隐私政策静态页面（通过 GitHub Pages 对外提供 HTTPS 访问，不依赖任何外部脚本或字体）。

> **安全红线**：**严禁向本公开仓库上传任何 `.keystore`、`.jks`、密码、私钥、签名文件或闭源游戏源码。**

## 目录结构与线上访问地址

```text
ppgiao123.github.io/
├── index.html                   # Play Console 开发者官网（MVP）
├── app-ads.txt                  # Google AdMob authorized seller 声明
└── ArrowGO/
    ├── index.html               # ArrowGO 游戏简介与支持页
    └── privacy/
        └── index.html           # ArrowGO 五语隐私政策（含 v1.10.2 AdMob + UMP 披露）
```

GitHub Pages 上线访问地址（注意路径区分大小写）：
- **开发者官网（MVP）**：`https://ppgiao123.github.io/`
- **AdMob `app-ads.txt`**：`https://ppgiao123.github.io/app-ads.txt`
- **ArrowGO 简介页**：`https://ppgiao123.github.io/ArrowGO/`
- **ArrowGO 隐私政策 URL**：`https://ppgiao123.github.io/ArrowGO/privacy/`

## Google Play Console 填写对照

仓库 **Settings -> Pages**（`https://github.com/PPgiao123/ppgiao123.github.io/settings/pages`）保持 `Deploy from a branch` -> `main` / `/ (root)`：
- **Store settings -> Website（开发者官网）**：`https://ppgiao123.github.io/`
- **App content -> Privacy policy（隐私政策 URL）**：`https://ppgiao123.github.io/ArrowGO/privacy/`

## 未来扩展其他游戏与 `app-ads.txt` 说明

- **新增游戏**：在仓库根目录新建对应游戏目录（例如 `ConquerGo/privacy/index.html`、`PlayWord/privacy/index.html`），并在根目录 `index.html` 增加游戏卡片链接即可。
- **`app-ads.txt`**：根目录 `app-ads.txt` 已配置 `pub-1727240179622631`，已在 `https://ppgiao123.github.io/app-ads.txt` 对外生效。
