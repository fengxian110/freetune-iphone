# FreeTune iPhone PWA（修复版）

## 本次修复
- 搜索按钮改为明确的点击事件，兼容 iPhone Safari。
- 搜索请求增加 12 秒超时，避免首次自动搜索卡住后一直无法再次搜索。
- Service Worker 缓存版本升级到 freetune-v3，便于手机获取新代码。
- 搜索仍使用 Openverse 开放许可音频 API；不破解会员、不抓取付费音乐。

## 更新到 GitHub Pages
1. 解压本 ZIP。
2. 将里面的 5 个文件上传到 GitHub 仓库根目录，覆盖同名文件。
3. 点击 Commit changes，等待 Pages 部署完成。
4. iPhone Safari 打开网站并刷新；若仍旧，关闭已添加到主屏幕的 FreeTune，删除图标，再从 Safari 重新添加。

## 注意
Openverse API 是免费开放许可媒体搜索服务，但服务可能限流或在部分网络环境无法访问。若显示“连接音乐曲库超时”，说明手机到 API 的网络请求未成功，并非搜索按钮失灵。
