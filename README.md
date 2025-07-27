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

> **Q:** How often should I water a snake plant?  
> **A:** Water every 2–3 weeks, allowing the soil to fully dry out between waterings. In winter, reduce watering frequency.

> **Q:** What causes yellowing leaves in pothos?  
> **A:** Overwatering is a common cause. Ensure the pot has good drainage, and let the top inch of soil dry before watering again.

These responses are generated using context pulled from the knowledge base — not from web searches or general training data.

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


## 📝 Lessons Learned

This project helped me:

- Deepen my understanding of LLM grounding and orchestration
- Explore semantic search and knowledge base construction
- Integrate multiple AWS services into a single working pipeline

---

## 🖼️ Demo or Screenshot

_(Add a screenshot or Loom video link here)_

---

## 📎 Related Repos / Links

- [Amazon Bedrock Docs](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html)
- [Claude Model Details](https://www.anthropic.com/index/claude)
