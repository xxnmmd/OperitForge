# SenseNova AI 创作平台

一个功能完整的图片生成、视频生成网站，基于商汤科技 SenseNova 大模型 API。

## 🎯 功能特性

### 🖼️ 图片生成
- 支持多种图片尺寸（1024×1024、1280×720、720×1280、2048×2048）
- 多种艺术风格选择（写实、动漫、油画、素描、3D 渲染）
- 可生成 1-4 张图片
- 实时进度显示
- 一键下载生成的图片

### 🎬 视频生成
- 支持多种视频时长（5秒、10秒、15秒）
- 多种视频尺寸（HD、Full HD、竖屏）
- 多种视频风格（电影质感、写实、动漫、3D 动画）
- 视频预览与下载

### 🔑 API 密钥管理
- **本地安全存储**：API 密钥保存在浏览器 localStorage 中，不会上传到任何服务器
- **独立密钥**：图片和视频生成可使用不同的 API 密钥
- **密钥查看**：支持查看/隐藏密钥
- **一键清除**：可安全清除已保存的密钥

### 📊 其他功能
- **生成历史**：自动保存最近 50 条生成记录
- **使用统计**：统计图片和视频生成次数
- **数据管理**：一键清除所有本地数据
- **快捷键支持**：Ctrl+Enter 快速生成
- **响应式设计**：完美适配桌面和移动设备

## 🚀 快速开始

### 1. 获取 API 密钥
访问 [https://token.sensenova.cn](https://token.sensenova.cn) 获取您的 SenseNova API 密钥

### 2. 配置密钥
1. 打开网站
2. 点击顶部导航栏的 **⚙️ 设置**
3. 在 "图片生成 API 密钥" 或 "视频生成 API 密钥" 输入框中粘贴您的密钥
4. 点击 **保存密钥** 按钮

### 3. 开始创作
1. 切换到 **🖼️ 图片生成** 或 **🎬 视频生成** 标签页
2. 在文本框中输入您的创作描述
3. 选择合适的参数（尺寸、风格、时长等）
4. 点击 **生成** 按钮
5. 等待生成完成，下载或保存到您的历史记录

## 📖 API 端点

| 功能 | 端点 | 方法 |
|------|------|------|
| 图片生成 | `/v1/images/generations` | POST |
| 视频生成 | `/v1/videos/generations` | POST |

### 请求示例

```javascript
// 图片生成
fetch('https://token.sensenova.cn/v1/images/generations', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer YOUR_API_KEY'
  },
  body: JSON.stringify({
    model: 'stable-diffusion',
    prompt: '一只可爱的猫咪在花园里玩耍',
    n: 1,
    size: '1024x1024',
    style: 'realistic'
  })
})

// 视频生成
fetch('https://token.sensenova.cn/v1/videos/generations', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer YOUR_API_KEY'
  },
  body: JSON.stringify({
    model: 'video-generation',
    prompt: '美丽的日落场景，海浪拍打沙滩',
    duration: 10,
    size: '1280x720',
    style: 'cinematic'
  })
})
```

## 🔒 安全说明

- ✅ API 密钥仅存储在本地浏览器中
- ✅ 密钥不会上传到任何第三方服务器
- ✅ 所有 API 请求直接发送到 SenseNova 官方端点
- ✅ 支持随时清除所有本地数据

## 📱 浏览器兼容性

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 🛠️ 技术栈

- **前端框架**：原生 HTML5 + CSS3 + JavaScript
- **图标库**：Font Awesome 6.4.0
- **数据存储**：localStorage
- **API 通信**：Fetch API

## 📝 使用提示

### 图片生成提示词技巧
```
好的提示词 = 主体 + 细节 + 风格 + 质量

示例：
- "一只可爱的金毛犬在阳光明媚的花园里奔跑，毛发细节清晰，写实风格，8K 画质"
- "赛博朋克风格的城市夜景，霓虹灯闪烁，雨后的街道，电影质感，高分辨率"
- "中国水墨画风格的山水，云雾缭绕，留白艺术，传统东方美学"
```

### 视频生成提示词技巧
```
好的视频提示词 = 场景 + 动作 + 氛围 + 技术参数

示例：
- "海浪轻轻拍打着金色沙滩，夕阳西下，天空呈现橙色和紫色渐变，电影质感，4K 画质，10 秒"
- "樱花花瓣在空中飘舞，春天公园场景，柔和光线，梦幻氛围，15 秒"
```

## 📞 支持

- 官方网站：[https://token.sensenova.cn](https://token.sensenova.cn)
- API 文档：[https://token.sensenova.cn/docs](https://token.sensenova.cn/docs)

## 📄 许可证

本项目为开源项目，可自由使用和修改。

---

**版本**: 1.0.0  
**最后更新**: 2024  
**开发者**: SenseNova AI Team
