# FudanEDG 项目结构规范

## 📁 项目目录结构

```
EGA_page/
├── index.html              # 主页面文件
├── README.md               # 项目说明文档
├── .gitignore              # Git忽略文件
├── assets/                 # 静态资源文件夹
│   ├── css/               # 样式文件
│   │   └── styles.css     # 主样式文件
│   ├── js/                # JavaScript文件
│   │   └── script.js      # 主脚本文件
│   ├── images/            # 图片资源
│   │   ├── logo/          # Logo图片
│   │   ├── team/          # 团队成员照片
│   │   ├── projects/      # 项目展示图片
│   │   ├── activities/    # 活动照片
│   │   └── backgrounds/   # 背景图片
│   ├── icons/             # 图标文件
│   │   ├── favicon.ico    # 网站图标
│   │   └── social/        # 社交媒体图标
│   └── fonts/             # 字体文件（如果需要本地字体）
├── docs/                  # 文档文件夹
│   ├── PROJECT_STRUCTURE.md  # 项目结构说明
│   ├── CONTENT_GUIDE.md      # 内容管理指南
│   └── DEPLOYMENT.md          # 部署指南
└── templates/             # 模板文件（如需要）
```

## 🖼️ 图片资源管理规范

### 图片分类和命名规范

#### 1. Logo图片 (`assets/images/logo/`)
- `logo-main.png` - 主Logo（推荐尺寸：200x60px）
- `logo-icon.png` - 图标版本（推荐尺寸：64x64px）
- `logo-dark.png` - 深色背景版本
- `logo-light.png` - 浅色背景版本

#### 2. 团队成员照片 (`assets/images/team/`)
- 命名格式：`member-{姓名拼音}.jpg`
- 推荐尺寸：300x300px
- 格式：JPG或PNG

#### 3. 项目展示图片 (`assets/images/projects/`)
- 命名格式：`project-{项目名称}-{序号}.jpg`
- 推荐尺寸：800x600px
- 格式：JPG

#### 4. 活动照片 (`assets/images/activities/`)
- 命名格式：`activity-{活动名称}-{日期}.jpg`
- 推荐尺寸：1200x800px
- 格式：JPG

#### 5. 背景图片 (`assets/images/backgrounds/`)
- `hero-bg.jpg` - 首页背景
- `section-bg-{序号}.jpg` - 各区块背景

### 图片优化建议

1. **文件大小**：单张图片不超过500KB
2. **格式选择**：
   - 照片：JPG格式
   - Logo/图标：PNG格式
   - 简单图形：SVG格式
3. **响应式图片**：为不同屏幕尺寸准备不同尺寸的图片

## 📝 内容管理指南

### 文字内容更新位置

1. **社团介绍** - 在`index.html`的`.about`部分
2. **活动方向** - 在`index.html`的`.activities`部分
3. **主要领域** - 在`index.html`的`.activity-areas`部分
4. **统计数据** - 在`index.html`的`.stats`部分
5. **联系信息** - 在`index.html`的`.footer`部分

### 添加新图片的步骤

1. 将图片放入对应的`assets/images/`子文件夹
2. 在HTML中使用相对路径引用：
   ```html
   <img src="assets/images/logo/logo-main.png" alt="FudanEDG Logo">
   ```
3. 更新CSS样式（如需要）

## 🚀 本地开发环境

### 启动本地服务器

#### 方法1: Python HTTP服务器
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
安装Live Server扩展，右键`index.html`选择"Open with Live Server"

### 开发工具推荐

- **代码编辑器**：VS Code
- **图片编辑**：Photoshop, GIMP, 或在线工具
- **版本控制**：Git
- **浏览器调试**：Chrome DevTools

## 📋 更新检查清单

在更新网站内容时，请检查：

- [ ] 所有图片路径正确
- [ ] 图片文件大小合理
- [ ] 文字内容准确无误
- [ ] 链接地址有效
- [ ] 移动端显示正常
- [ ] 浏览器兼容性良好

## 🔧 技术规范

### HTML规范
- 使用语义化标签
- 保持代码缩进一致
- 添加适当的alt属性

### CSS规范
- 使用BEM命名规范
- 保持样式模块化
- 响应式设计优先

### JavaScript规范
- 使用ES6+语法
- 添加错误处理
- 保持代码可读性
