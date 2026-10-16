# binthere 简体中文前端

此版本基于 `detesion/binthere` 的 main 分支，将网页默认语言改为简体中文。

已汉化创建、分享、密码设置与确认、解密、阅后即焚、复制、删除、倒计时、错误提示、公告及无障碍标签；补充系统中文字体回退。品牌名、算法名、Markdown、原作者外链和英文文档保留。原分享预览图片未重新绘制。

## 应用修改

修改的运行文件只有以下五个：

- `public/index.html`
- `public/css/styles.css`
- `public/js/app.js`
- `public/js/ui.js`
- `public/js/stars.js`

加密协议、后端接口、Cloudflare 资源绑定及 CLI 保持原样。

如果使用 `binthere-zh-CN-files.zip`，解压后在 GitHub 的 `detesion/binthere` 仓库选择 **Add file → Upload files**，将解压后的 `public` 文件夹与本说明上传至仓库根目录，保持子目录层级，提交至 `main`。

如果使用本地 Git，请先完成自己的 GitHub 授权，再提交并推送以上文件。无需在聊天中提供密码或访问令牌。

## 部署

若 Cloudflare 已连接该仓库并启用 main 分支自动部署，推送后等待部署成功即可。否则在 Cloudflare 中手动触发部署，或在已完成 Cloudflare 登录的本地环境运行 `npm run deploy`。

本次汉化不会创建或替换 KV、Durable Object 资源。自定义域名确定后，仍需按上游 README 的 Self-hosting 说明更新页面的 Open Graph URL 和 security.txt 中的地址。

## 验证

- `npm run lint` 通过。
- `npm test` 通过：Worker 136 项、DOM 41 项、CLI 149 项，共 326 项。
- 本地浏览器验证中文页面、空内容校验、密码确认、错误密码与正确密码解密、阅后即焚提示。

以上为本地验证，尚未推送到 GitHub 或部署到 Cloudflare。
