# FudanEDG 内容管理指南

## 📝 内容更新指南

### 1. 社团基本信息更新

#### 社团名称和描述
**位置**：`index.html` 第15-20行
```html
<h1 class="hero-title">FudanEDG</h1>
<h2 class="hero-subtitle">探索电子创客的无限可能，创造智能未来</h2>
<p class="hero-description">
    <!-- 在这里更新社团描述 -->
</p>
```

#### 统计数据更新
**位置**：`index.html` 第85-95行
```html
<div class="stat-item">
    <h3>50+</h3>
    <p>完成项目</p>
</div>
<div class="stat-item">
    <h3>100+</h3>
    <p>活跃成员</p>
</div>
<div class="stat-item">
    <h3>20+</h3>
    <p>技术讲座</p>
</div>
```

### 2. 活动方向内容更新

#### 主要活动卡片
**位置**：`index.html` 第45-65行
```html
<div class="activity-card">
    <h3>电子设计</h3>
    <p>从基础电路到复杂系统，掌握电子设计的核心技能</p>
</div>
```

### 3. 主要领域内容更新

#### 领域卡片内容
**位置**：`index.html` 第120-180行
```html
<div class="area-card">
    <h3>硬件设计</h3>
    <p>电路设计、PCB制作、硬件调试等基础技能培养</p>
    <ul>
        <li>基础电路设计</li>
        <li>PCB设计与制作</li>
        <li>硬件调试技术</li>
    </ul>
</div>
```

### 4. 社团亮点更新

#### 亮点卡片
**位置**：`index.html` 第200-230行
```html
<div class="highlight-card">
    <h3>创新项目</h3>
    <p>我们完成了多个具有实用价值的创新项目，从智能家居到机器人系统，展现创客精神。</p>
</div>
```

## 🖼️ 图片添加指南

### 1. 添加Logo图片

#### 在导航栏添加Logo
**位置**：`index.html` 第12-15行
```html
<div class="nav-logo">
    <img src="assets/images/logo/logo-main.png" alt="FudanEDG Logo" class="logo-img">
    <span class="logo-text">FudanEDG</span>
</div>
```

#### 在首页添加Logo
**位置**：`index.html` 第20行后
```html
<div class="hero-logo">
    <img src="assets/images/logo/logo-main.png" alt="FudanEDG Logo" class="hero-logo-img">
</div>
```

### 2. 添加项目展示图片

#### 在项目卡片中添加图片
```html
<div class="activity-card">
    <img src="assets/images/projects/project-arduino-1.jpg" alt="Arduino项目" class="card-image">
    <h3>电子设计</h3>
    <p>从基础电路到复杂系统，掌握电子设计的核心技能</p>
</div>
```

### 3. 添加活动照片

#### 在活动区域添加背景图片
```html
<div class="activities" style="background-image: url('assets/images/backgrounds/activities-bg.jpg');">
    <!-- 活动内容 -->
</div>
```

## 🎨 样式自定义指南

### 1. 修改主题颜色

**位置**：`assets/css/styles.css`

#### 主色调修改
```css
:root {
    --primary-color: #2563eb;    /* 主色调 */
    --secondary-color: #667eea;  /* 辅助色 */
    --accent-color: #764ba2;     /* 强调色 */
}
```

#### 渐变背景修改
```css
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### 2. 修改字体

**位置**：`index.html` 第8行
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

### 3. 修改布局间距

**位置**：`assets/css/styles.css`
```css
section {
    padding: 80px 0;  /* 修改区块间距 */
}

.container {
    max-width: 1200px;  /* 修改容器宽度 */
}
```

## 📱 响应式设计检查

### 移动端适配检查点

1. **导航菜单**：在小屏幕上是否正常折叠
2. **图片显示**：是否自适应屏幕大小
3. **文字大小**：是否在移动端清晰可读
4. **按钮大小**：是否适合触摸操作

### 测试方法

1. 使用浏览器开发者工具的设备模拟器
2. 在不同设备上实际测试
3. 检查不同屏幕尺寸下的显示效果

## 🔗 链接和联系方式更新

### 1. 社交媒体链接

**位置**：`index.html` 第240-250行
```html
<div class="footer-section">
    <h4>联系我们</h4>
    <ul>
        <li><a href="https://github.com/fudanedg">GitHub</a></li>
        <li><a href="mailto:contact@fudanedg.com">Email</a></li>
        <li><a href="#">微信群</a></li>
    </ul>
</div>
```

### 2. 申请加入链接

**位置**：`index.html` 第220行
```html
<a href="mailto:join@fudanedg.com" class="btn btn-primary">申请加入</a>
```

## ✅ 更新检查清单

在更新网站内容后，请检查：

- [ ] 所有文字内容准确无误
- [ ] 图片路径正确且图片正常显示
- [ ] 链接地址有效
- [ ] 移动端显示正常
- [ ] 浏览器兼容性良好
- [ ] 页面加载速度正常
- [ ] SEO元数据完整

## 🚀 部署前检查

1. **本地测试**：使用本地服务器测试所有功能
2. **图片优化**：确保图片文件大小合理
3. **代码检查**：确保没有语法错误
4. **链接测试**：确保所有链接正常工作
5. **移动端测试**：在不同设备上测试显示效果
