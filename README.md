# BAR FRATI 全新点餐网站 V2

## 功能
- 在这里吃（Mangiare qui）：无需桌号
- 外带（Da asporto）：填写取餐时间、可选姓名
- 中意双语菜单，32道菜，主食可加肉/虾各 +€1
- 前台提交，后厨通过 Socket.IO 实时接收
- 后厨点击「开启来单铃声」，页面保持打开时新单重复提醒，可确认停止
- 订单状态：新订单、制作中、完成

## 新建 GitHub 仓库（不要改旧仓库）
1. GitHub -> New repository，名称例如 `bar-frati-new`，选择 Public，Create repository。
2. 点击 uploading an existing file，打开本压缩包**解压后的 BAR_FRATI_全新网站 文件夹**，把 `server.js`、`package.json`、`README.md` 和 `public` 文件夹**一起拖入**上传区域（需确认列表出现 `public/index.html`）。
3. 点击 Commit changes。

## 新建 Render 服务
1. Render -> New -> Web Service -> 选择新的 GitHub 仓库。
2. Runtime: Node；Build command: `npm install`；Start command: `npm start`；Free（仅测试）。
3. 部署成功后打开 Render 提供的全新 URL。
4. 前台：`https://你的新网址/#front`；后厨：`https://你的新网址/#kitchen`。

## 重要限制
- Render Free 可能休眠，造成订单延迟。
- Free 服务的本地文件不是持久数据库，重启或重新部署可能丢失订单、菜单修改。
- 当前没有用户登录或权限控制；知道网址的人可能查看/修改订单或菜单，切勿直接用于正式营业。
- iPhone Safari 锁屏/后台不能保证响铃；后厨需保持页面可见、屏幕亮起并手动启用铃声。
