# 🐍 贪吃蛇游戏 (Snake Game)

一个基于 HTML5 Canvas 的经典贪吃蛇游戏，具有精美的 UI 设计和流畅的游戏体验。

![Snake Game](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

## 🌟 功能特性

### 核心功能
- ✅ **经典贪吃蛇玩法** - 经典的贪吃蛇游戏机制
- ✅ **实时计分系统** - 实时显示当前得分和最高分
- ✅ **最高分记录** - 使用 localStorage 保存最高分
- ✅ **暂停功能** - 按 空格键暂停/继续游戏

### UI/UX 设计
- 🎨 **精美界面** - 渐变背景和现代化设计
- 📱 **响应式设计** - 支持桌面和移动设备
- 🎮 **触摸控制** - 支持移动端滑动操作
- 📊 **清晰反馈** - 游戏结束和暂停提示

### 技术亮点
- 🚀 **纯原生实现** - 无任何外部依赖
- ⚡ **高性能渲染** - 使用 HTML5 Canvas API
- 📦 **单文件部署** - 所有代码在一个 HTML 文件中
- 🔧 **易于扩展** - 代码结构清晰，方便修改

## 🎮 游戏玩法

### 控制方式

#### 桌面端
- **方向键** ↑ ↓ ← → - 控制蛇的移动方向
- **空格键** - 暂停/继续游戏

#### 移动端
- **滑动屏幕** - 在游戏区域滑动控制蛇的移动方向

### 游戏规则
1. 蛇通过吃掉食物来增长
2. 每吃掉一个食物得 10 分
3. 撞到墙壁或自己的身体则游戏结束
4. 尝试获得最高分！

## 🚀 快速开始

### 方法一：直接打开
1. 下载 `snake-game.html` 文件
2. 双击打开或拖入浏览器
3. 开始游戏！

### 方法二：本地服务器
```bash
# 使用 Python 3
python -m http.server 8000

# 使用 Node.js
npx serve

# 使用 PHP
php -S localhost:8000
```
然后访问 `http://localhost:8000/snake-game.html`

### 方法三：GitHub Pages
1. Fork 或克隆本仓库
2. 在 GitHub 上启用 GitHub Pages
3. 访问 `https://yourusername.github.io/snake-game`

## 📸 游戏截图

![Snake Game Screenshot](https://via.placeholder.com/400x400/667eea/ffffff?text=Snake+Game)

## 🛠️ 技术实现

### 核心技术
- **HTML5 Canvas** - 游戏渲染
- **CSS3** - 样式和动画
- **JavaScript (ES6+)** - 游戏逻辑

### 代码结构
```
snake-game.html
├── HTML 结构
├── CSS 样式
└── JavaScript 逻辑
    ├── 游戏配置
    ├── 游戏状态管理
    ├── 输入处理
    ├── 渲染逻辑
    └── 碰撞检测
```

### 关键功能实现

#### 游戏循环
```javascript
setInterval(draw, gameSpeed); // 游戏主循环
```

#### 碰撞检测
```javascript
// 撞墙检测
if (head.x < 0 || head.x >= tileCount || head.y < 0 || head.y >= tileCount)

// 自身碰撞检测
snake.some(segment => segment.x === head.x && segment.y === head.y)
```

#### 触摸控制
```javascript
canvas.addEventListener('touchstart', handleTouchStart);
canvas.addEventListener('touchend', handleTouchEnd);
```

## 🎯 自定义选项

### 修改游戏速度
在 JavaScript 代码中找到：
```javascript
const gameSpeed = 100; // 毫秒，数值越小速度越快
```

### 修改游戏网格大小
```javascript
const gridSize = 20; // 网格大小（像素）
const tileCount = canvas.width / gridSize; // 网格数量
```

### 修改蛇的颜色
```javascript
// 蛇头
ctx.fillStyle = '#4CAF50';

// 蛇身
ctx.fillStyle = '#8BC34A';
```

### 修改食物颜色
```javascript
ctx.fillStyle = '#FF5722';
```

## 📊 性能优化

- ✅ 使用 `requestAnimationFrame` 替代 `setInterval`（可优化）
- ✅ 减少 DOM 操作，使用 Canvas 批量渲染
- ✅ 优化碰撞检测算法
- ✅ 使用 CSS3 硬件加速

## 🌐 浏览器兼容性

- ✅ Chrome (推荐)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ 移动端浏览器

## 📝 更新日志

### v1.0.0 (2026-02-14)
- ✨ 初始版本发布
- 🎮 实现核心贪吃蛇玩法
- 🎨 添加精美 UI 设计
- 📱 支持触摸控制
- 💾 添加最高分记录功能

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 如何贡献
1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- 感谢所有贡献者
- 感谢 GitHub 提供代码托管服务

## 📧 联系方式

- 项目链接：https://github.com/Joshualover/snake-game
- 作者：Joshualover

---

⭐ 如果你觉得这个项目有用，请给它一个 Star！
