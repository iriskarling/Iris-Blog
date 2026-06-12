# AI 产品经理个人博客

这是一个适合部署到阿里云 OSS 或 GitHub Pages 的静态作品集站点。

## 当前目录结构

- `index.html`：主页
- `404.html`：错误页，默认跳回首页
- `style.css`：主页样式
- `script.js`：主页交互动效
- `caixiaofu_data_agent_api_demo_atomic_metric_api_no_extra_column.html`：内测案例 1
- `project_showcase_onepage_with_demo_prompt_mapping_v2.html`：内测案例 2
- `CNAME`：GitHub Pages 自定义域名配置
- `.nojekyll`：关闭 Jekyll 处理，按纯静态站点发布

## 已完成的静态站点准备

- 已使用相对路径，适合直接上传到仓库根目录
- 已移除 Google Fonts 等国外前端依赖，更适合国内访问
- 已添加 `404.html`，便于配置 OSS 错误页
- 已保留 `CNAME` 和 `.nojekyll`，仅在 GitHub Pages 场景下使用

## 阿里云 OSS 部署方式

1. 在阿里云创建一个 OSS Bucket
2. 地域优先选择离目标用户更近的国内节点
3. 将 Bucket 权限按你的实际需求设置
4. 开启 `静态页面` 功能
5. 默认首页设置为 `index.html`
6. 默认 404 / 错误页设置为 `404.html`
7. 将当前目录中的站点文件全部上传到 Bucket 根目录
8. 如果需要绑定自定义域名，再在 OSS / CDN 和阿里云 DNS 中配置域名解析

## GitHub Pages 部署方式

1. 新建一个 GitHub 仓库
2. 将当前目录全部文件上传到仓库根目录
3. 在 GitHub 仓库 `Settings > Pages` 中开启 GitHub Pages
4. 选择 `Deploy from a branch`
5. 分支选择 `main`，目录选择 `/root`

## 域名说明

当前 `CNAME` 文件已写入：

`iriswang.com.cn`

说明：

- 如果你使用 GitHub Pages，`CNAME` 文件会生效
- 如果你使用阿里云 OSS，`CNAME` 文件不会影响站点运行，可以保留，也可以忽略
- 如果你后续想改成 `www.iriswang.com.cn`，只需要把 `CNAME` 文件内容改成对应域名即可

## 本地预览

直接双击 `index.html` 即可在浏览器中预览主页。
