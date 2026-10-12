# StarAttract Aggregate AI Demo
星引聚合 AI，一站式大模型聚合平台。一套 API 调用多款顶尖大模型，降低接入成本，支持企业、开发者批量使用。

> One-stop LLM aggregation platform. One API to access multiple top-tier large models, reducing integration costs, supporting bulk usage for enterprises and developers.

## 接口基础信息
- 接口地址：`https://xingyunyinli.com/v1/chat/completions`
- 鉴权方式：Bearer Token
- 兼容 OpenAI 接口格式

## 1. cURL 调用示例
```bash
curl "https://xingyunyinli.com/v1/chat/completions" \
  -H "Authorization: Bearer $XY_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"your-model","messages":[{"role":"user","content":"你好"}]}'

## Python 调用示例

import requests

api_key = "YOUR_API_KEY"
url = "https://xingyunyinli.com/v1/chat/completions"

resp = requests.post(
    url,
    headers={
        "Authorization": f"Bearer {api_key}",
        "Content-Type": "application/json"
    },
    json={
        "model": "your-model",
        "messages": [{"role": "user", "content": "你好"}]
    }
)
print(resp.json())

## Node.js 调用示例
const fetch = require('node-fetch');

const apiKey = "YOUR_API_KEY";
const url = "https://xingyunyinli.com/v1/chat/completions";

fetch(url, {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${apiKey}`,
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    model: "your-model",
    messages: [{role: "user", content: "你好"}]
  })
}).then(res=>res.json()).then(data=>console.log(data));
