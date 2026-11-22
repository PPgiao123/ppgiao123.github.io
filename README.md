# PPgiao123 游戏官网、公开落地页与隐私政策仓库 (`ppgiao123.github.io`)

本公开仓库用于托管 **PPgiao123** 旗下游戏的海外落地页、游戏简介页、Google AdMob `app-ads.txt` 与隐私政策静态页面（通过 GitHub Pages 对外提供 HTTPS 访问，零外部字体或第三方重型依赖，支持手机端社媒内置浏览器秒开）。

> **安全红线**：**严禁向本公开仓库上传任何 `.keystore`、`.jks`、密码、私钥、签名文件或闭源游戏源码。**

## 目录结构与线上访问地址

```text
ppgiao123.github.io/
├── index.html                        # ArrowGO 海外主落地页 & PPgiao123 开发者官网
├── app-ads.txt                       # Google AdMob authorized seller 声明
├── assets/
│   └── arrowgo/
│       ├── icon.png                  # ArrowGO 512x512 应用图标
│       ├── feature-graphic.png       # 1024x500 主视觉与 Open Graph 分享卡片图
│       ├── shot-untangle.png         # Level 15 Grand Untangle 实机截图
│       ├── shot-heart.png            # Level 06 心形棋盘实机截图
│       ├── shot-keylock.png          # Level 07 钥匙锁链实机截图
│       ├── shot-hub.png              # 45 关与每日/随机模式实机截图
│       └── shot-duel.png             # 本地双人 / 三档 AI 分屏对战截图
└── ArrowGO/
    ├── index.html                    # ArrowGO 游戏详情页
    └── privacy/
        └── index.html                # ArrowGO 五语隐私政策（含 v1.10.2 AdMob + UMP 披露）
```

GitHub Pages 上线访问地址（注意路径区分大小写）：
- **开发者官网 / ArrowGO 主落地页**：`https://ppgiao123.github.io/`
- **AdMob `app-ads.txt`**：`https://ppgiao123.github.io/app-ads.txt`
- **ArrowGO 详情页**：`https://ppgiao123.github.io/ArrowGO/`
- **ArrowGO 隐私政策 URL**：`https://ppgiao123.github.io/ArrowGO/privacy/`

## Google Play Console 填写对照

仓库 **Settings -> Pages**（`https://github.com/PPgiao123/ppgiao123.github.io/settings/pages`）保持 `Deploy from a branch` -> `main` / `/ (root)`：
- **Store settings -> Website（开发者官网）**：`https://ppgiao123.github.io/`
- **App content -> Privacy policy（隐私政策 URL）**：`https://ppgiao123.github.io/ArrowGO/privacy/`

## 10 秒切换上线链接（Google Play / Poki / CrazyGames / 社媒）

在 `index.html` 与 `ArrowGO/index.html` 底部 `<script>` 顶部的 `ARROWGO_LINKS` 对象中直接填入真实链接即可（留空时会自动展示 Beta 测试申请或敬请期待弹窗，绝无死链）：

```js
var ARROWGO_LINKS = {
  googlePlayUrl: "https://play.google.com/store/apps/details?id=com.ppgiao123.arrowgo",
  webPlayUrl: "https://poki.com/en/g/arrowgo", // 或 CrazyGames 链接
  xUrl: "https://x.com/your_handle",
  instagramUrl: "https://instagram.com/your_handle",
  youtubeUrl: "https://youtube.com/@your_handle"
};
```

## 2 分钟接入免费每日访客与社媒渠道统计（Cloudflare Web Analytics）

GitHub Pages 本身**不提供**网站每日访客统计（GitHub 仓库 `Insights -> Traffic` 只统计代码仓库页面访问，不含 `ppgiao123.github.io` 网站访客）。推荐直接使用 **Cloudflare Web Analytics**（**免费、无需购买独立域名、无需修改 DNS、无 Cookie 免弹窗**）：

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/) -> 左侧 **Analytics & Logs** -> **Web Analytics** -> 点击 **Add a site**。
2. 站点主机名填写 `ppgiao123.github.io`，复制生成的那 1 行 `<script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "..."}'></script>`。
3. 打开 `index.html` 与 `ArrowGO/index.html` 最底部注释的 `Cloudflare Web Analytics` 占位行，替换为你的 Token 并取消注释，提交推送即可。
4. **区分各社媒导流效果技巧**：在社媒发不同来源的链接，后台就能按 `Path / Query` 和 `Referrer` 分别统计每天点击量与设备（iOS / Android / Desktop）：
   - X (Twitter)：`https://ppgiao123.github.io/?src=x`
   - Instagram：`https://ppgiao123.github.io/?src=ig`
   - YouTube：`https://ppgiao123.github.io/?src=yt`

## 未来扩展其他游戏与 `app-ads.txt` 说明

- **新增游戏**：在仓库根目录新建对应游戏目录（例如 `ConquerGo/privacy/index.html`、`PlayWord/privacy/index.html`），并在根目录 `index.html` 预留的注释块取消注释即可。
- **`app-ads.txt`**：根目录 `app-ads.txt` 已配置 `pub-1727240179622631`，已在 `https://ppgiao123.github.io/app-ads.txt` 对外生效。
