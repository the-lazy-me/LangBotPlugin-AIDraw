# 图片生成插件 (img-plugin)

这是一个支持 OpenAI 兼容 API 的 LangBot 图片生成插件，支持自定义模型和服务提供商。

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

2. 配置 API 参数：
   - 复制 `.env.example` 为 `.env`
   - 填入你的 API 配置信息

3. 在 LangBot 中配置插件参数：
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
- `https://api.openai.com/v1` (OpenAI 官方，默认)
- `https://api.deepseek.com/v1` (DeepSeek)
- 其他兼容 OpenAI 格式的服务地址

### model (可选)
图片生成模型名称，例如：
- `dall-e-3` (默认)
- `dall-e-2`
- 其他支持的模型名称

### image_size (可选)
支持的尺寸：
- `1024x1024` (正方形，默认)
- `1792x1024` (横向)
- `1024x1792` (竖向)

## 注意事项

1. 需要有效的 API Key
2. 图片生成需要消耗 API 额度
3. 请遵守相应服务提供商的使用条款和内容政策
4. 确保使用的 API 服务兼容 OpenAI 图片生成接口格式
