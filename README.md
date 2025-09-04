# 图片生成插件 (img-plugin)

这是一个支持 OpenAI 兼容 API 的 LangBot 图片生成插件。

## 功能特性

- 支持中英文命令触发图片生成
- 兼容 OpenAI 图片生成 API 格式
- 支持自定义 API 服务地址和模型
- 可配置图片尺寸
- 支持群聊和私聊

## 安装配置

1. 安装依赖：
```bash
pip install -r requirements.txt
```

2. 在 LangBot WebUI 中配置插件参数：
   - `api_key`: 图片生成服务的 API 密钥 (必需)
   - `base_url`: API 服务地址 (可选，默认 OpenAI)
   - `model`: 图片生成模型名称 (可选，默认 dall-e-3)
   - `image_size`: 图片尺寸 (可选，默认 1024x1024)

## 使用方法

支持以下命令触发图片生成：
- `画图 [描述]`
- `生成图片 [描述]`
- `draw [描述]`
- `image [描述]`

示例：
- `画图 一只可爱的小猫在花园里玩耍`
- `draw a beautiful sunset over the ocean`

## 配置参数

### api_key (必需)
图片生成服务的 API 密钥

### base_url (可选)
API 服务的基础地址，支持：
- `https://api.qhaigc.net/v1` (默认绘图地址)
- 其他兼容 OpenAI 格式的服务地址

### model (可选)
图片生成模型名称，例如：
- `qh-draw-x1-pro` (默认)

### image_size (可选)
支持的尺寸：
- `1024x1024` (正方形，默认)
- `1792x1024` (横向)
- `1024x1792` (竖向)
