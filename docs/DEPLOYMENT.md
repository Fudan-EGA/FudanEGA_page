# FudanEDG 部署指南

## 🚀 GitHub Pages 部署

### 1. 准备工作

#### 创建GitHub仓库
1. 登录GitHub
2. 点击"New repository"
3. 仓库名称建议：`fudanedg-website` 或 `fudanedg.github.io`
4. 设置为Public（GitHub Pages免费版需要）
5. 不要初始化README（因为已有文件）

### 2. 上传项目文件

#### 方法1: 使用Git命令行
```bash
# 进入项目目录
cd /Users/ningzhang/lanyun/EGA_page

# 初始化Git仓库
git init

# 添加所有文件
git add .

# 提交更改
git commit -m "Initial commit: FudanEDG website"

# 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/yourusername/fudanedg-website.git

# 推送到GitHub
git push -u origin main
```

#### 方法2: 使用GitHub Desktop
1. 下载并安装GitHub Desktop
2. 选择"Clone a repository from the Internet"
3. 输入你的仓库URL
4. 将项目文件复制到克隆的文件夹
5. 提交并推送更改

#### 方法3: 直接上传文件
1. 在GitHub仓库页面点击"uploading an existing file"
2. 拖拽项目文件夹中的所有文件
3. 添加提交信息并提交

### 3. 启用GitHub Pages

1. 进入仓库的"Settings"页面
2. 滚动到"Pages"部分
3. 在"Source"下选择"Deploy from a branch"
4. 选择"main"分支和"/ (root)"文件夹
5. 点击"Save"

### 4. 访问网站

部署完成后，你的网站将在以下地址可用：
- `https://yourusername.github.io/fudanedg-website`
- 或 `https://fudanedg.github.io`（如果仓库名为fudanedg.github.io）

## 🔧 本地开发环境

### 启动本地服务器

#### 方法1: Python HTTP服务器（推荐）
```bash
cd /Users/ningzhang/lanyun/EGA_page
python3 -m http.server 8000
```
访问：`http://localhost:8000`

#### 方法2: Node.js serve
```bash
cd /Users/ningzhang/lanyun/EGA_page
npx serve .
```

#### 方法3: VS Code Live Server
1. 安装"Live Server"扩展
2. 右键点击`index.html`
3. 选择"Open with Live Server"

#### 方法4: 其他本地服务器
```bash
# 使用PHP
php -S localhost:8000

# 使用Ruby
ruby -run -e httpd . -p 8000
```

### 开发工具推荐

- **代码编辑器**：VS Code
- **浏览器**：Chrome（用于调试）
- **版本控制**：Git + GitHub Desktop
- **图片编辑**：Photoshop, GIMP, 或在线工具

## 📁 项目文件管理

### 文件组织结构
```
EGA_page/
├── index.html              # 主页面
├── README.md               # 项目说明
├── .gitignore              # Git忽略文件
├── assets/                 # 静态资源
│   ├── css/
│   ├── js/
│   ├── images/
│   ├── icons/
│   └── fonts/
├── docs/                   # 文档
└── templates/              # 模板（如需要）
```

### 图片资源管理

#### 图片分类
- `assets/images/logo/` - Logo文件
- `assets/images/team/` - 团队成员照片
- `assets/images/projects/` - 项目展示图片
- `assets/images/activities/` - 活动照片
- `assets/images/backgrounds/` - 背景图片

#### 图片优化建议
1. **文件大小**：单张图片不超过500KB
2. **格式选择**：
   - 照片：JPG格式
   - Logo/图标：PNG格式
   - 简单图形：SVG格式
3. **命名规范**：使用英文和连字符，如`project-arduino-1.jpg`

## 🔄 更新和部署流程

### 日常更新流程

1. **本地修改**
   ```bash
   # 修改文件后
   git add .
   git commit -m "Update: 描述你的更改"
   git push origin main
   ```

2. **自动部署**
   - GitHub Pages会自动检测更改
   - 通常在几分钟内更新网站

3. **验证更新**
   - 访问网站确认更改生效
   - 检查移动端显示
   - 测试所有链接

### 批量更新流程

1. **准备更新内容**
   - 整理所有需要更新的文字
   - 准备新的图片资源
   - 检查链接地址

2. **本地测试**
   - 使用本地服务器测试
   - 检查所有功能正常
   - 验证响应式设计

3. **提交部署**
   - 提交所有更改
   - 推送到GitHub
   - 等待自动部署完成

## 🛠️ 故障排除

### 常见问题

#### 1. 网站无法访问
- 检查GitHub Pages设置
- 确认仓库为Public
- 等待几分钟让部署完成

#### 2. 图片不显示
- 检查图片路径是否正确
- 确认图片文件已上传
- 检查文件名大小写

#### 3. 样式不生效
- 检查CSS文件路径
- 清除浏览器缓存
- 检查CSS语法错误

#### 4. 移动端显示异常
- 使用浏览器开发者工具
- 检查响应式CSS规则
- 测试不同屏幕尺寸

### 调试工具

1. **浏览器开发者工具**
   - F12打开开发者工具
   - 检查Console错误信息
   - 使用Network标签检查资源加载

2. **在线工具**
   - [W3C HTML验证器](https://validator.w3.org/)
   - [W3C CSS验证器](https://jigsaw.w3.org/css-validator/)
   - [Google PageSpeed Insights](https://pagespeed.web.dev/)

## 📊 性能优化

### 图片优化
1. **压缩图片**：使用TinyPNG等工具
2. **使用适当格式**：JPG用于照片，PNG用于透明图片
3. **响应式图片**：为不同屏幕准备不同尺寸

### 代码优化
1. **压缩CSS/JS**：使用在线工具压缩
2. **合并文件**：减少HTTP请求
3. **使用CDN**：加速资源加载

### 加载速度优化
1. **懒加载**：图片延迟加载
2. **预加载**：关键资源预加载
3. **缓存策略**：设置适当的缓存头

## 🔒 安全考虑

### 基本安全措施
1. **HTTPS**：GitHub Pages自动提供HTTPS
2. **内容安全**：避免在代码中暴露敏感信息
3. **链接安全**：确保所有外部链接安全

### 隐私保护
1. **个人信息**：避免在网站中暴露个人隐私
2. **联系方式**：使用社团邮箱而非个人邮箱
3. **图片权限**：确保使用的图片有适当权限
