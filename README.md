# 离线URL图床

将任意图片编码为 `data:` URL，**纯前端、零依赖、完全离线可用**。

双击 `index.html` 即可使用，不需要任何服务器。

## 功能

- 🖱️ 拖拽图片 / 点击选择 / Ctrl+V 粘贴截图
- 🔗 直接生成 `data:image/格式;base64,...` URL
- 📋 一键复制，粘贴到浏览器地址栏即可显示
- 👀 实时预览 + 编码统计

## 支持格式

PNG · JPEG · GIF · WebP · SVG · BMP

## 使用

```bash
# 方式一：直接双击
index.html

# 方式二：浏览器打开
打开 index.html # macOS
启动 index.html # Windows
```

将生成的 `data:` URL 粘贴到：
- 浏览器地址栏 → 直接显示图片
- HTML `<img src="...">` → 嵌入网页
- Markdown `![](data:...)` → 嵌入文档
- 任何支持 base64 图片的地方

## 原理

```
图片文件 → FileReader → base64编码 → data:image/png;base64,xxxx
                                         ↑
                                    离线URL，无需服务器
```
