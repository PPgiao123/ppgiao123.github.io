# PPgiao123 工作室官网、应用矩阵与隐私政策仓库 (`ppgiao123.github.io`)

本公开仓库用于托管 **PPgiao123** 旗下全部应用的开发者主页、各款游戏的独立海外落地页、Google AdMob `app-ads.txt` 与隐私政策静态页面（通过 GitHub Pages 对外提供 HTTPS 访问，零外部字体或第三方重型依赖，支持手机端社媒内置浏览器秒开）。

> **安全红线**：**严禁向本公开仓库上传任何 `.keystore`、`.jks`、密码、私钥、签名文件或闭源游戏源码。**

## 双层结构与线上访问地址

```text
ppgiao123.github.io/
├── index.html                        # PPgiao123 全部应用官网主页（Studio Hub）
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
    ├── index.html                    # ArrowGO 完整海外落地页（社媒导流主落点）
    └── privacy/
        └── index.html                # ArrowGO 五语隐私政策（含 v1.10.2 AdMob + UMP 披露）
```

GitHub Pages 上线访问地址（注意路径区分大小写）：
- **PPgiao123 全部应用官网主页（适合放社交账号主页 Bio / Play Console Website）**：`https://ppgiao123.github.io/`
- **ArrowGO 完整海外落地页（适合发 ArrowGO 宣传视频/帖子附带）**：`https://ppgiao123.github.io/ArrowGO/`
- **ArrowGO 隐私政策 URL**：`https://ppgiao123.github.io/ArrowGO/privacy/`
- **AdMob `app-ads.txt`**：`https://ppgiao123.github.io/app-ads.txt`

## Google Play Console 填写对照

仓库 **Settings -> Pages**（`https://github.com/PPgiao123/ppgiao123.github.io/settings/pages`）保持 `Deploy from a branch` -> `main` / `/ (root)`：
- **Store settings -> Website（开发者官网）**：`https://ppgiao123.github.io/`
- **App content -> Privacy policy（隐私政策 URL）**：`https://ppgiao123.github.io/ArrowGO/privacy/`

## 10 秒切换上线链接（Google Play / Poki / CrazyGames / 社媒）

在 `ArrowGO/index.html` 底部 `<script>` 顶部的 `ARROWGO_LINKS` 对象中直接填入真实链接即可（留空时会自动展示 Beta 测试申请或敬请期待弹窗，绝无死链）；根目录 `index.html` 的 `STUDIO_LINKS` 可填写工作室社媒主页链接：

```js
var ARROWGO_LINKS = {
  googlePlayUrl: "https://play.google.com/store/apps/details?id=com.ppgiao123.arrowgo",
  webPlayUrl: "https://poki.com/en/g/arrowgo", // 或 CrazyGames 链接
  xUrl: "https://x.com/your_handle",
  instagramUrl: "https://instagram.com/your_handle",
  youtubeUrl: "https://youtube.com/@your_handle"
};
```

## 如何添加未来的新应用 / 新游戏

1. 新建目录 `MyNewApp/`（放置该应用的落地页 `index.html` 与隐私政策 `MyNewApp/privacy/index.html`）以及素材目录 `assets/mynewapp/`。
2. 在根目录 `index.html` 的 `.apps-grid` 中参考注释模板追加一个 `<article class="app-card">` 卡片即可（可将 `More Apps Coming Soon` 卡片留在末尾或移除）。
3. 根目录 `app-ads.txt` 由同开发者账号下的所有应用共用；如接入新广告渠道按需追加行。

## 2 分钟接入免费每日访客与社媒渠道统计（Cloudflare Web Analytics）

GitHub Pages 本身**不提供**网站每日访客统计（GitHub 仓库 `Insights -> Traffic` 只统计代码仓库页面访问，不含 `ppgiao123.github.io` 网站访客）。推荐直接使用 **Cloudflare Web Analytics**（**免费、无需购买独立域名、无需修改 DNS、无 Cookie 免弹窗**）：

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/) -> 左侧 **Observability / Analytics & Logs** -> **Web Analytics** -> 点击 **Add a site**。
2. Hostname 填写 `ppgiao123.github.io`，点击 **Done**，复制第 2 步生成的 `<script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "..."}'></script>`。
3. 将同一个 Token 同时替换并取消注释到根目录 `index.html` 和 `ArrowGO/index.html`（以及未来所有新增子应用页）最底部的 `Cloudflare Web Analytics` 占位块，提交推送即可在同一个 Cloudflare 看板看到全站及各子路径的每日数据。
4. **区分各社媒导流效果技巧**：
   - 发 ArrowGO 专属推文/短视频时可分别使用：
     - X：`https://ppgiao123.github.io/ArrowGO/?src=x`
     - Instagram：`https://ppgiao123.github.io/ArrowGO/?src=ig`
     - YouTube：`https://ppgiao123.github.io/ArrowGO/?src=yt`
   - 社媒账号主页 Bio 放工作室总入口：`https://ppgiao123.github.io/`
