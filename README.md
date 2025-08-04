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

| Category | Examples | Use Cases |curl -X POST "https://api.neuralnets.link" \
  -H "Content-Type: application/json" \
  -H "x-api-key: sk-ce420d58262144d8a5389606ac486bc904e2a6c547f9464a94bac2e879044326" \
  -d '{
    "model": "qwen/qwen3-30b-a3b",
    "messages": [
      {
        "role": "user",
        "content": [
          {
            "type": "text",
            "text": "Explain quantum mechanics to a 5 year old."
          }
        ]
      }
    ],
    "reasoning": { "effort": "medium" }
  }'
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

| Tier | Monthly Requests | Price | Features |
|------|-----------------|-------|----------|
| 🆓 **Free** | 1,000 | $0 | Basic models, community support |
| 🚀 **Pro** | 100,000 | $29 | All models, priority support |
| 🏢 **Enterprise** | Unlimited | Custom | SLA, custom models, dedicated support |

> 💡 **[View Detailed Pricing →](https://neuranets.link/pricing)**

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

| Channel | Response Time | Availability |
|---------|---------------|--------------|
| 📧 Email | 24 hours | support@neuranets.link |
| 💬 Live Chat | Instant | Business hours |
| 📚 Documentation | Always | docs.neuranets.link |
| 🐛 Issues | 48 hours | GitHub Issues |

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. 🍴 Fork the repository
2. 🌿 Create a feature branch
3. ✨ Make your changes
4. 🧪 Add tests
5. 📝 Update documentation
6. 🚀 Submit a pull request

See our [Contributing Guide](CONTRIBUTING.md) for detailed instructions.

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE.md](LICENSE.md) file for details.

---

<div align="center">

### 🌟 Star us on GitHub if you find NeuralNets.link helpful!

**Made with ❤️ by the NeuralNets.link Team**

[Website](https://neuranets.link) • [Documentation](https://docs.neuranets.link) • [Status Page](https://status.neuranets.link) • [Blog](https://blog.neuranets.link)

</div>
