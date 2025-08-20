# GitHub Pages 部署指南

## 快速部署步骤

### 1. 创建 GitHub 仓库
1. 访问 [GitHub](https://github.com) 并登录
2. 点击右上角的 "+" 号，选择 "New repository"
3. 仓库名建议：`zjy-tech-website` 或 `revit-plugins-site`
4. 设置为 **Public**（GitHub Pages 免费版需要公开仓库）
5. 不要勾选 "Initialize this repository with a README"
6. 点击 "Create repository"

### 2. 上传网站文件

**方法一：使用 GitHub 网页界面（推荐新手）**
1. 在新创建的仓库页面，点击 "uploading an existing file"
2. 将以下文件拖拽到上传区域：
   - `index.html`
   - `styles.css`
   - `script.js`
   - `README.md`
3. 在底部填写提交信息：`Initial commit: ZJY Tech Studio website`
4. 点击 "Commit changes"

**方法二：使用 Git 命令行**
```bash
# 在网站文件夹中打开命令行，执行以下命令：
git init
git add .
git commit -m "Initial commit: ZJY Tech Studio website"
git branch -M main
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

### 3. 启用 GitHub Pages
1. 在仓库页面，点击 "Settings" 标签
2. 在左侧菜单中找到 "Pages"
3. 在 "Source" 部分：
   - 选择 "Deploy from a branch"
   - Branch 选择 "main"
   - Folder 选择 "/ (root)"
4. 点击 "Save"

### 4. 访问网站
- 网站地址：`https://你的用户名.github.io/你的仓库名/`
- 部署通常需要 5-10 分钟
- GitHub 会在 Pages 设置页面显示网站 URL

## 自定义域名（可选）

如果您有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容只写您的域名，如：`www.zjytech.com`
3. 在域名提供商处设置 DNS：
   - 添加 CNAME 记录：`www` 指向 `你的用户名.github.io`
   - 或添加 A 记录指向 GitHub Pages IP

## 更新网站

每次修改网站内容后：

1. 直接在 GitHub 网页上编辑文件，或
2. 使用 Git 命令推送更新：
```bash
git add .
git commit -m "Update website content"
git push
```

## 网站功能检查清单

部署后请检查：
- [ ] 网站能正常访问
- [ ] 导航菜单工作正常
- [ ] 响应式设计在手机上显示正确
- [ ] 联系表单能正常提交（会显示感谢消息）
- [ ] 3D 动画正常播放
- [ ] 所有链接都能正常工作

## 常见问题

**Q: 网站显示 404 错误**
A: 检查 GitHub Pages 设置，确保选择了正确的分支和文件夹

**Q: 样式没有加载**
A: 检查文件路径，确保 CSS 和 JS 文件在正确位置

**Q: 网站更新没有生效**
A: GitHub Pages 有缓存，可能需要等待几分钟或强制刷新浏览器

**Q: 想要 HTTPS**
A: GitHub Pages 自动提供 HTTPS，在设置中启用 "Enforce HTTPS"

## 后续优化建议

1. **添加 Google Analytics** 跟踪访问数据
2. **设置联系表单后端** 使用 Formspree 或 Netlify Forms
3. **添加博客功能** 使用 Jekyll 或其他静态站点生成器
4. **优化 SEO** 提交到 Google Search Console
5. **添加多语言支持** 中英文切换功能

## 技术支持

如需技术支持或定制开发，请联系 ZJY Tech Studio。
