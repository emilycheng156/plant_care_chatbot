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


## ⚙️ Architecture

- **Amazon S3** stores plant care documents in `.txt`, `.pdf`, and `.md` formats
- **Knowledge Base** uses semantic embedding and vector similarity search
- **Bedrock Agent** generates responses grounded in the retrieved content
- All components are no-code/low-code using AWS services

---

## 🧪 Sample Interaction

**User:**  
> How often should I water my monstera plant?

**Bot:**  
> Monstera prefers its soil to dry out between waterings. Water every 1–2 weeks depending on the humidity and light levels. Reduce frequency in winter.

(*Backed by retrieved S3 documents on tropical plant care.*)

---

## 🧰 Tech Stack

| Component     | Technology                      |
|---------------|----------------------------------|
| LLM           | Amazon Bedrock (Claude 3 Sonnet) |
| Retrieval     | Bedrock Knowledge Bases          |
| Vector DB     | Amazon OpenSearch                |
| Document Store| Amazon S3                        |
| Language/API  | Python (Boto3)                   |

---

## 📈 Key Features

- ✅ Retrieval-augmented generation (RAG) over custom documents
- ✅ Claude 3 model integration with zero infrastructure setup
- ✅ Dynamic answers from personalized plant data
- ✅ Modular architecture (easy to extend with symptom diagnosis or image input)

---

## 📌 Next Steps

- [ ] Add web-based frontend using Lambda + API Gateway  
- [ ] Enable user-uploaded plant care PDFs  
- [ ] Fine-tune embedding chunking and scoring thresholds  

---

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
