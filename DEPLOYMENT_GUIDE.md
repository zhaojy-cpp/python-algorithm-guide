# GitHub Pages 部署指南

## 🚀 快速部署步骤

### 方法一：使用GitHub网页界面（推荐新手）

1. **创建GitHub账户**（如果还没有）
   - 访问 https://github.com
   - 注册新账户

2. **创建新仓库**
   - 点击右上角的 "+" → "New repository"
   - 仓库名称：`python-algorithm-guide`（或你喜欢的名字）
   - 选择 "Public"（GitHub Pages需要公开仓库）
   - 不要初始化README
   - 点击 "Create repository"

3. **上传文件**
   - 在新仓库页面，点击 "uploading an existing file"
   - 拖拽或选择本目录下的所有HTML文件
   - 等待上传完成
   - 点击 "Commit changes"

4. **启用GitHub Pages**
   - 进入仓库的 "Settings" 标签
   - 左侧菜单找到 "Pages"
   - 在 "Source" 部分：
     - 选择 "Deploy from a branch"
     - 选择 "main" 分支
     - 选择 "/ (root)" 文件夹
   - 点击 "Save"

5. **访问你的网站**
   - 等待几分钟（GitHub需要时间来部署）
   - 访问 `https://[your-username].github.io/[repo-name]`
   - 例如：`https://alice.github.io/python-algorithm-guide`

### 方法二：使用Git命令行（推荐开发者）

1. **安装Git**
   - 下载地址：https://git-scm.com/downloads

2. **初始化本地仓库**
   ```bash
   cd /path/to/your/files
   git init
   git add .
   git commit -m "Initial commit"
   ```

3. **创建GitHub仓库并连接**
   ```bash
   # 创建新仓库（在GitHub网站上操作）
   # 然后复制仓库URL，例如：
   git remote add origin https://github.com/yourusername/your-repo-name.git
   git branch -M main
   git push -u origin main
   ```

4. **启用GitHub Pages**（同方法一步骤4）

## 📋 部署前检查清单

- [ ] 所有HTML文件都已上传
- [ ] index.html位于根目录
- [ ] 仓库设置为Public
- [ ] GitHub Pages已启用并配置正确
- [ ] 等待部署完成（通常2-10分钟）

## 🔧 常见问题解决

### 1. 网站显示404错误
- **原因**：GitHub Pages还未完成部署
- **解决**：等待5-10分钟后刷新页面

### 2. 样式显示不正确
- **原因**：可能是CSS或字体加载失败
- **解决**：
  - 检查网络连接
  - 确认Tailwind CSS CDN链接有效
  - 清除浏览器缓存

### 3. 点击卡片无反应
- **原因**：JavaScript可能被浏览器阻止
- **解决**：
  - 确保使用HTTPS访问
  - 检查浏览器控制台错误信息
  - 尝试使用不同浏览器

### 4. 中文显示乱码
- **原因**：字符编码问题
- **解决**：确认所有HTML文件都有`<meta charset="UTF-8">`

## 🎨 自定义网站

### 修改网站标题
编辑 `index.html` 文件：
```html
<title>你的网站标题 - Python算法竞赛指南</title>
```

### 添加自己的Logo
在 `slide01.html` 中替换Logo图片链接：
```html
<img src="你的logo链接" alt="Logo">
```

### 修改颜色主题
所有幻灯片都使用Tailwind CSS，可以轻松修改颜色类名。

## 📊 网站分析

可以添加Google Analytics来跟踪访问数据：

1. 注册Google Analytics账户
2. 获取跟踪ID（GA4）
3. 在每个HTML文件的`<head>`部分添加跟踪代码

## 🔒 安全建议

1. **保持仓库Public**：GitHub Pages免费版需要公开仓库
2. **不要上传敏感信息**：如API密钥、密码等
3. **定期更新依赖**：检查CDN链接是否仍然有效
4. **使用HTTPS**：GitHub Pages自动提供HTTPS

## 📞 获取帮助

如果遇到问题：

1. 查看GitHub Pages文档：https://docs.github.com/en/pages
2. 检查本项目的Issues（如果公开的话）
3. 在GitHub社区寻求帮助

---

**祝你部署成功！** 🚀✨