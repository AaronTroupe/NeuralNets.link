<div align="center">

# NeuralNets.link

**Unified API for AI Models**

*Access 250+ AI models from 50+ providers through a single, powerful API*

[![API Status](https://img.shields.io/badge/API-Live-brightgreen)](https://api.neuranets.link)
[![Models](https://img.shields.io/badge/Models-250+-blue)](https://neuranets.link/models)
[![Providers](https://img.shields.io/badge/Providers-50+-purple)](https://neuranets.link/providers)
[![License](https://img.shields.io/badge/License-API%20License-red)](LICENSE.md)

[🚀 Get Started](https://neuralnets.link/login) • [📖 Documentation](https://neuralnets.link/documentation) • [🆘 Support](https://discord.com/invite/TGNMBASxYa)

</div>

---

<div align="center">

## 🎯 What is NeuralNets.link?

NeuralNets.link is a **unified API platform** that provides seamless access to over **250 AI models** from more than **50 leading providers**. We simplify AI integration for developers and businesses by offering a single, standardized interface to interact with diverse AI capabilities.

### 🔥 Key Features

<table>
<tr>
<td align="center">🔗<br><strong>Unified API</strong><br>One API for all models</td>
<td align="center">⚡<br><strong>High Performance</strong><br>Optimized for scale</td>
<td align="center">💡<br><strong>Easy Integration</strong><br>Switch models instantly</td>
<td align="center">💰<br><strong>Cost Effective</strong><br>Pay only what you use</td>
</tr>
</table>

</div>

---

## 🚀 Getting Started

### 1️⃣ Sign Up
Create your account at [NeuralNets.link](https://neuralnets.link/login)

### 2️⃣ Get Your API Key
Get your API key from the [dashboard](https://neuralnets.link/dashboard)

### 3️⃣ Make Your First Request
```bash
curl -X POST "https://api.neuralnets.link" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
    "model": "YOUR_MODEL_CHOICE",
    "messages": [
      {
        "role": "user",
        "content": [
          {
            "type": "text",
            "text": "Hello, world!"
          }
        ]
      }
    ]
  }'
```

---

## 🛠️ Usage Examples

### 🐍 Python
```python
import requests

# Configuration
API_KEY = "your_api_key_here"
MODEL_ID = "your_model_choice"
BASE_URL = "https://api.neuralnets.link"

# Headers
headers = {
    "Content-Type": "application/json",
    "x-api-key": API_KEY
}

# Prepare request data
data = {
    "model": MODEL_ID,
    "messages": [
        {
            "role": "user",
            "content": [
                {
                    "type": "text",
                    "text": "Explain quantum computing in simple terms"
                }
            ]
        }
    ]
}

# Make request
response = requests.post(BASE_URL, headers=headers, json=data)

# Handle response
if response.status_code == 200:
    result = response.json()
    print(result)
else:
    print(f"Error: {response.status_code} - {response.text}")
```

### 🟨 JavaScript/Node.js
```javascript
const API_KEY = "your_api_key_here";
const MODEL_ID = "your_model_choice";
const BASE_URL = "https://api.neuralnets.link";

async function callModel(message) {
    const requestData = {
        model: MODEL_ID,
        messages: [
            {
                role: "user",
                content: [
                    {
                        type: "text",
                        text: message
                    }
                ]
            }
        ]
    };

    try {
        const response = await fetch(BASE_URL, {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
                "x-api-key": API_KEY
            },
            body: JSON.stringify(requestData)
        });

        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }

        const data = await response.json();
        return data;
    } catch (error) {
        console.error('API call failed:', error);
        throw error;
    }
}

// Usage
callModel("Write a haiku about artificial intelligence")
    .then(result => console.log(result))
    .catch(error => console.error(error));
```

---

## 🤖 Available Models

We provide access to cutting-edge AI models across multiple categories:

| Category | Examples | Use Cases |
|----------|----------|-----------|
| 💬 **Text Generation** | GPT-4, Claude, PaLM | Content creation, chatbots, writing assistance |
| 🖼️ **Image Recognition** | CLIP, ResNet, EfficientNet | Image classification, object detection |
| 🗣️ **Natural Language** | BERT, RoBERTa, T5 | Sentiment analysis, text classification |
| 🌐 **Translation** | mT5, MarianMT | Multi-language translation |

---

## 🔐 Authentication

All API requests require authentication using your API key in the `x-api-key` header. You can get your API key from the [dashboard](https://neuralnets.link/dashboard).

```http
x-api-key: YOUR_API_KEY
```

### 🛡️ Security Best Practices

- ✅ Keep your API key secret
- ✅ Use HTTPS for all requests
- ✅ Rotate keys regularly
- ✅ Monitor usage in your dashboard

---

## 📊 Response Format

All API responses follow the OpenAI-compatible structure:

```json
{
  "id": "82560878-19a0-c49f-ebe7-bd6cafdbafc4",
  "object": "chat.completion",
  "created": 1754397150,
  "model": "gpt-4",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Your AI-generated response here...",
        "refusal": null
      },
      "finish_reason": "stop"
    }
  ],
  "usage": {
    "prompt_tokens": 28,
    "completion_tokens": 150,
    "total_tokens": 178,
    "prompt_tokens_details": {
      "text_tokens": 28,
      "audio_tokens": 0,
      "image_tokens": 0,
      "cached_tokens": 5
    },
    "completion_tokens_details": {
      "reasoning_tokens": 0,
      "audio_tokens": 0,
      "accepted_prediction_tokens": 0,
      "rejected_prediction_tokens": 0
    },
    "num_sources_used": 0
  },
  "system_fingerprint": "fp_0d42a4eb3d"
}
```

---

## 💰 Pricing

For detailed pricing information for all models, access the models tab in [neuralnets.link/dashboard](https://neuralnets.link/dashboard) or simply hit the GET API endpoint [neuralnets.link/api/models](https://neuralnets.link/api/models) to see all models pricing.

## 🆘 Support

Need help? Join our Discord community at [https://discord.com/invite/TGNMBASxYa](https://discord.com/invite/TGNMBASxYa) for support and discussions.

---

## 📄 License

This service is governed by the **NeuralNets.link API License Agreement**. While our backend infrastructure remains proprietary, developers are granted commercial usage rights to build applications using our API services.

### API License Summary

**✅ What You Can Do:**
- Build commercial applications using our API
- Integrate our services into your products
- Resell applications that use our API
- Use our API for business purposes

**❌ What You Cannot Do:**
- Access, reverse engineer, or copy our backend code
- Redistribute or resell direct API access
- Use the service for illegal or harmful content
- Exceed rate limits or attempt to circumvent restrictions

**📋 Key Terms:**
- **Service License**: Non-exclusive right to use our API services
- **Commercial Use**: Full commercial rights for applications built with our API
- **Data Ownership**: You retain ownership of your input data and own the API output
- **Usage Limits**: Subject to rate limits and fair use policies
- **Support**: Best-effort support through our official channels

For complete terms, see our [API License Agreement](https://neuranets.link/license) and [Terms of Service](https://neuranets.link/terms).
