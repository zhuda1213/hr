# 红星招聘 · 前台 H5 + 管理后台原型

红星实业集团招聘平台的静态高保真原型，纯单文件 HTML，无构建、无外部依赖，打开即用。

## 页面

| 路径 | 说明 |
| --- | --- |
| `/`（`index.html`） | 候选人移动端 H5：首页、职位、职位详情、投递、我的简历、投递记录、登录注册 |
| `/admin/` | HR 管理后台：数据看板、岗位管理、候选人管理、人才库、黑名单、账号与角色权限、系统设置 |

## 演示账号

- **H5**：手机号 `13856789211`，验证码固定 `888888`（演示环境不做真实下发）。也可在登录弹层点「使用演示账号」一键进入。
- **管理后台**：邮箱任意（默认 `hr-admin@redstar-hr.com`），密码任意（默认 `123456`）。

## 说明

- 数据仅存在浏览器 `localStorage`（H5 使用 key `hx_h5_v1`），刷新保留、换设备/换浏览器不共享，属于纯前端原型，不对接后端。
- 「我的 → 重置演示数据」可把 H5 恢复为初始种子数据。
- 后台建议用桌面浏览器访问（≥1280px），H5 建议用手机或 DevTools 移动视图（390px）查看。

## 静态托管说明

本仓库根目录即站点根目录：`/` 是 H5，`/admin/` 是管理后台，已放置 `.nojekyll`。

**Gitee Pages 不可用**：该服务已于 2024 年 5 月下线，仓库存放代码可以，但无法生成 `*.gitee.io` 访问地址（实测 404），也不能直接打开仓库里的 HTML。

当前线上演示（内置托管）：

| 端 | 地址 |
| --- | --- |
| H5 | `https://hongxing-recruit.app.workbuddy.host/?sharecode=HXHQD6QC2B` |
| 管理后台 | `https://hongxing-recruit.app.workbuddy.host/admin/?sharecode=HXHQD6QC2B` |

可选托管方式：

| 方式 | 操作 | 地址形态 |
| --- | --- | --- |
| GitHub Pages | 本仓库 → Settings → Pages → Source 选 `Deploy from a branch` → 分支 `main`，目录 `/ (root)` | `https://<用户名>.github.io/<仓库名>/` |
| Cloudflare Pages | 连接 Git 仓库，构建命令留空，输出目录填 `/` | `https://<项目>.pages.dev/` |
| 任意对象存储 / 静态服务器 | 把仓库文件原样上传到站点根目录即可 | 自有域名 |
| 本地查看 | 直接双击 `index.html`（H5），或 `python -m http.server` 起本地服务 | `http://localhost:8000/` |
