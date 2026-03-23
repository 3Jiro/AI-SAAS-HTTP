# 🕸️ Intelligent Web-to-SaaS Content Pipeline
### 🌟 Overview
An automated content engine that leverages HTTP-based web ingestion and multi-stage LLM processing to transform raw HTML into structured visual and text assets for a SaaS environment.

### 🛠️ Technical Architecture
- **Dynamic HTML Parsing:** Custom-built selectors to strip boilerplate code and focus on the core semantic content of a webpage.

- **Multi-Model Pipeline:** A "Strategy Model" generates the creative direction, while a "Polishing Model" refines the final prompt for image generation.

- **Webhook Delivery:** Engineered as a stateless API that accepts a URL and returns a generated asset (Image + Copy) in under 30 seconds.

### 🚀 Key Challenges Overcome
- **Content Hallucination:** Added a validation step that compares the generated output against the original source text to ensure factual alignment.

- **Rate-Limit Management:** Implemented "Wait" states and asynchronous processing to handle high-latency image generation APIs without timing out the webhook.

### ⚙️ Tech stack
- **Primary Engine:** n8n (self hosted) / HTTP
- **AI/LLM:** Gemini / OpenAI / DALL-E
- **Data & storage:** HTML Parser
- **Communication:** Webhook
