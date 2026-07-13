# 职工电子工牌 · GitHub Pages 部署说明

按 [GitHub Pages 官方文档](https://docs.github.com/en/pages) 操作即可把本文件夹变成**永久网址**。

## 一、准备（只需做一次）

1. 打开 [https://github.com](https://github.com) 注册 / 登录账号  
2. 电脑已安装 Git（本机已有即可）

## 二、在 GitHub 上新建仓库

1. 打开 [https://github.com/new](https://github.com/new)  
2. **Repository name** 填：`employee-badge`（可改）  
3. 选 **Public**（免费 Pages 要求公开仓库，或使用有权限的私有方案）  
4. **不要**勾选 “Add a README”  
5. 点 **Create repository**

创建后页面会显示你的仓库地址，形如：

`https://github.com/你的用户名/employee-badge.git`

## 三、把本文件夹推送到 GitHub

在 PowerShell 中执行（把 `你的用户名` 换成真实用户名）：

```powershell
cd F:\Seurat_umap_export\employee_badge_gh

git init
git add .
git commit -m "Publish employee badge site"
git branch -M main
git remote add origin https://github.com/你的用户名/employee-badge.git
git push -u origin main
```

推送时浏览器会弹出 GitHub 登录 / 授权，按提示完成即可。

## 四、打开 GitHub Pages

1. 打开仓库页面 → **Settings** → 左侧 **Pages**  
2. **Source** 选 **Deploy from a branch**  
3. **Branch** 选 `main`，文件夹选 `/ (root)`  
4. 点 **Save**  

等待约 1 分钟，页面顶部会出现网址，一般是：

**`https://你的用户名.github.io/employee-badge/`**

这就是永久链接。手机浏览器打开、扫码、或「添加到主屏幕」都可以。

## 五、以后如何更新页面

改完 `index.html` 或图片后，在本目录执行：

```powershell
cd F:\Seurat_umap_export\employee_badge_gh
git add .
git commit -m "Update badge"
git push
```

几分钟后线上会自动更新。

## 说明

- 本目录已包含 `.nojekyll`，避免 GitHub 用 Jekyll 错误处理静态资源  
- 永久链接不依赖电脑开机  
- 详细官方说明见：[Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
