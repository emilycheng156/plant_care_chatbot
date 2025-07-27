# 🌿 Plant Care Chatbot with Amazon Bedrock

## 🔍 Overview
A natural language chatbot that provides accurate and personalized plant care advice by retrieving relevant information from a custom-built knowledge base. This project leverages **Amazon Bedrock** Agents with **retrieval-augmented generation (RAG)** to enable seamless Q&A over user-curated content.

---

## 🔍 Problem

Most plant care advice online is **fragmented**, **overly generalized**, or **buried in forums and blog posts**. You often have to sift through dozens of pages to answer simple but specific questions like:

- How much light does a pothos actually need?
- Why are my monstera leaves curling?
- What soil mix should I use for succulents?

Search results may contradict each other, lack scientific grounding, or assume conditions that don’t apply to your home. The result is confusion, trial-and-error, and unhealthy plants.

---

## 💡 Solution

I built a **Retrieval-Augmented Generation (RAG) chatbot** using **Amazon Bedrock** that gives accurate, consistent answers to plant care questions — sourced from structured, vetted horticultural documents.

Instead of scraping the internet, this chatbot retrieves relevant content from a **predefined plant care knowledge base** and uses a foundation model to generate clear, helpful responses.

---

## 🧠 How It Works

- 📄 **Amazon S3** holds structured plant care docs (PDFs, guides, etc.)
- 🧠 **Titan Text Embeddings v2** converts documents into semantic vectors
- 🔍 **Amazon OpenSearch Serverless** stores and retrieves embeddings
- 🤖 **Amazon Bedrock Agent** (LLaMA 3.3 70B) answers questions using retrieved content

This RAG architecture ensures that every answer is grounded in reliable source material — no hallucination, no guesswork.
## 💬 Example Interactions


<img width="303" height="497" alt="Screenshot 2025-07-27 at 3 55 18 PM" src="https://github.com/user-attachments/assets/82a252b9-b30d-444f-a7d7-e1891c292936" />

In this example, the chatbot answers “What causes yellowing leaves in pothos?” with a clear, in-depth explanation that’s actually useful. Instead of just listing possible causes, it explains the most common ones—like overwatering, root rot, and nutrient deficiencies—and even tells you how to check for root rot by looking at the condition of the roots. Unlike a regular Google search, which would return a list of blogs, forums, and websites you have to sift through yourself, this chatbot delivers a direct, trustworthy response in one place. It also cites the exact sources it used, so you know where the information came from and can get further details if needed.

---


## 🧰 Technologies Used

| Component             | Service / Model                     |
|----------------------|--------------------------------------|
| Foundation Model     | Meta LLaMA 3.3 70B (Bedrock)         |
| Embedding Model      | Titan Text Embeddings v2             |
| Vector Store         | Amazon OpenSearch Serverless         |
| File Storage         | Amazon S3                            |
| Orchestration Layer  | Amazon Bedrock Agent + Knowledge Base|

---

## 🌱 Why This Matters

By combining **semantic search** with **natural language generation**, this chatbot makes plant care knowledge accessible, specific, and trustworthy — all without requiring users to know the right keywords or source.

It’s a practical example of how RAG can be used to deliver **niche, reliable AI answers** in a noisy online world.

---

## 📝 Summary

This project shows how to build a specialized, high-accuracy chatbot by:
- Applying Retrieval-Augmented Generation (RAG)
- Using Bedrock’s serverless infrastructure
- Focusing on high-quality, domain-specific knowledge

It’s a foundation for scalable, trustworthy AI applications — from plant care to tech support and beyond.

## 📈 Key Features

- ✅ Retrieval-augmented generation (RAG) over custom documents
- ✅ Claude 3 model integration with zero infrastructure setup
- ✅ Dynamic answers from personalized plant data
- ✅ Modular architecture (easy to extend with symptom diagnosis or image input)




## 📎 Related Links

- [Amazon Bedrock Docs](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html)
- [Claude Model Details](https://www.anthropic.com/index/claude)
