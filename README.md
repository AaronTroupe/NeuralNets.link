# 🧠 NeuralNets.link

<div align="center">

**Unified API for AI Models**

*Access 250+ AI models from 50+ providers through a single, powerful API*

[![API Status](https://img.shields.io/badge/API-Live-brightgreen)](https://api.neuranets.link)
[![Models](https://img.shields.io/badge/Models-250+-blue)](https://neuranets.link/models)
[![Providers](https://img.shields.io/badge/Providers-50+-purple)](https://neuranets.link/providers)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE.md)

[🚀 Get Started](#-getting-started) • [📖 Documentation](https://docs.neuranets.link) • [💰 Pricing](https://neuranets.link/pricing) • [🆘 Support](#-support)

</div>

---

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

---

## 🚀 Getting Started

### 1️⃣ Sign Up
Create your account at [NeuralNets.link](https://neuranets.link)

### 2️⃣ Get Your API Key
Navigate to your dashboard and copy your API key

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
    ],
    "reasoning": { "effort": "medium" }
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
    ],
    "reasoning": {"effort": "medium"}
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
        ],
        reasoning: { effort: "medium" }
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
| 🎨 **Image Generation** | DALL-E, Midjourney, Stable Diffusion | Creative content, art generation |
| 🔊 **Audio Processing** | Whisper, WaveNet | Speech-to-text, audio synthesis |

> 📋 **[View Complete Model Catalog →](https://neuranets.link/models)**

---

## 🔐 Authentication

All API requests require authentication using your API key in the `x-api-key` header:

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

All API responses follow a consistent structure:

```json
{
  "success": true,
  "model": "gpt-4",
  "usage": {
    "tokens": 150,
    "cost": 0.003
  },
  "output": "Your AI-generated response here...",
  "metadata": {
    "request_id": "req_abc123",
    "processing_time": 1.2
  }
}
```

---

## 💰 Pricing

For detailed pricing information for all models, access the models tab in [neuralnets.link/dashboard](https://neuralnets.link/dashboard) or simply hit the GET API endpoint [neuralnets.link/api/models](https://neuralnets.link/api/models) to see all models pricing.

---

## 📚 Resources

### 📖 Documentation
- [API Reference](https://docs.neuranets.link/api)
- [Model Guides](https://docs.neuranets.link/models)
- [Integration Examples](https://docs.neuranets.link/examples)
- [SDKs & Libraries](https://docs.neuranets.link/sdks)

### 🎓 Tutorials
- [Getting Started Guide](https://docs.neuranets.link/getting-started)
- [Best Practices](https://docs.neuranets.link/best-practices)
- [Common Use Cases](https://docs.neuranets.link/use-cases)

---

## 🆘 Support

Need help? We're here for you!

Visit our documentation at [neuralnets.link/documentation](https://neuralnets.link/documentation), or access the support Discord for any questions or issues at [https://discord.com/invite/TGNMBASxYa](https://discord.com/invite/TGNMBASxYa)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE.md](LICENSE.md) file for details.

---

<div align="center">
