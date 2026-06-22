# n8n Automated Workflows

A collection of [n8n](https://n8n.io) workflows built for AI-powered media generation, advertising intelligence, virtual try-on, and brand trend analysis. Each workflow is documented with a screenshot in the [`workflows/`](workflows/) folder.

## Workflows

| Workflow | Description | Screenshot |
|----------|-------------|------------|
| **Chanel Workflow** | Brand trend intelligence pipeline. Gathers research and competitor signals in parallel, merges them, then runs trend clustering, scoring, and a final release recommendation. | [chanel-workflow.png](workflows/chanel-workflow.png) |
| **Ad Intelligence** | Advertising trend analysis workflow. Collects research and competitor signals, clusters trends, scores them, and outputs a final trend release recommendation. | [ad-intelligence-workflow.png](workflows/ad-intelligence-workflow.png) |
| **Media Gen** | Multi-modal media generation via webhook. Uses AI agents (Google Vertex) to classify requests and route to image, audio, or video generation paths before responding. | [media-gen-workflow.png](workflows/media-gen-workflow.png) |
| **Multimodal Content** | Webhook-driven content pipeline with query and media classifiers. Routes requests to image, audio, or video generation branches powered by Google Gemini. | [multimodal-content-workflow.png](workflows/multimodal-content-workflow.png) |
| **Chat-Based PMAX Campaign Image Generator** | Conversational workflow for Google Ads Performance Max campaigns. Validates chat input with a Gemini agent, then generates logo, landscape, square, and portrait images. | [chat-based-pmax-campaign-image-generator-workflow.png](workflows/chat-based-pmax-campaign-image-generator-workflow.png) |
| **Virtual Try-On** | Google AI Hackathon virtual try-on workflow. Accepts webhook input, processes images from multiple angles via parallel HTTP and JavaScript branches, and returns results. | [Virtual-Try-On.png](workflows/Virtual-Try-On.png) |
| **Wardrobe Intelligence** | Wardrobe saved assets API. Webhook with GET (fetch from Google Cloud Storage) and POST (upload and transform) paths, both responding via a single webhook node. | [Wardrobe-intelligence.png](workflows/Wardrobe-intelligence.png) |

## Repository Structure

```
.
├── README.md
└── workflows/
    ├── ad-intelligence-workflow.png
    ├── chanel-workflow.png
    ├── chat-based-pmax-campaign-image-generator-workflow.png
    ├── media-gen-workflow.png
    ├── multimodal-content-workflow.png
    ├── Virtual-Try-On.png
    └── Wardrobe-intelligence.png
```

## Technologies Used

- **n8n** — workflow automation and orchestration
- **Google Gemini / Vertex AI** — LLM agents for classification and generation
- **HTTP Request nodes** — external API integrations
- **Webhooks** — real-time triggers and responses
- **JavaScript (Code nodes)** — custom data transformation logic

## Getting Started

1. Install and run [n8n](https://docs.n8n.io/hosting/).
2. Review the workflow screenshots in [`workflows/`](workflows/) to understand each pipeline.
3. Recreate or import the workflows in your n8n instance and configure credentials (Google AI, cloud storage, etc.).

> **Note:** This repository contains workflow screenshots for documentation. Export your `.json` workflow files from n8n to version-control the full definitions.
