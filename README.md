# FreeTune — iPhone 免费音乐播放器

一个可添加到 iPhone 主屏幕的 PWA。使用 Openverse Audio API 搜索音乐，并仅请求 Openverse 标记为开放许可的音乐作品（CC0、PDM、CC BY 等）。本项目不托管音乐文件、不破解会员或 DRM。

## 本地预览

直接打开 `index.html` 可以查看界面；浏览器通常要求 HTTPS/localhost 才允许 PWA 安装和 Service Worker。推荐部署到 HTTPS 静态托管。

## 部署到 GitHub Pages

1. 登录 GitHub，新建一个公开仓库，例如 `freetune-iphone`。
2. 上传本目录中的 `index.html`、`manifest.webmanifest`、`sw.js`、`icon.svg`。
3. 仓库 Settings → Pages → Deploy from a branch，选择 `main` 和 `/ (root)` 保存。
4. 等待 GitHub Pages 发布，得到 `https://你的用户名.github.io/freetune-iphone/` 地址。

也可以使用 Netlify / Cloudflare Pages 的静态站点部署功能，发布本目录即可。

## iPhone 安装

1. 用 iPhone 的 Safari 打开部署网址（不要用微信内置浏览器）。
2. 点击底部“分享”按钮。
3. 选择“添加到主屏幕”。
4. 点击“添加”，桌面会出现 FreeTune 图标。

## 曲库和许可说明

- 搜索接口：`https://api.openverse.org/v1/audio/`
- Openverse 是开放许可媒体搜索引擎，匿名访问有速率限制。
- 应用筛选音乐类别，并包含 CC0、PDM、CC BY 等许可类型。
- 许可并不等于所有用途均无限制：CC BY/SA 等可能要求署名或相同方式共享；NC 表示非商业；ND 表示不得改编。播放、下载、再利用前请进入作品来源页核对具体条款。
- Openverse 的结果可能包含无法直接播放的音源、失效链接或跨域限制；遇到无法播放的曲目可尝试其他结果，并从作品来源页访问。
- 此版本为第一版原型：在线搜索、播放、上一首/下一首、播放状态和 PWA 基础缓存已实现。收藏、歌词、离线下载、曲库账号等尚未实现。

## 文件

- `index.html`：界面与播放器逻辑
- `manifest.webmanifest`：PWA 安装信息
- `sw.js`：基础静态资源缓存
- `icon.svg`：应用图标
