# 🌿 Plant Care Chatbot with Amazon Bedrock

## 🔍 Overview
A natural language chatbot that provides accurate and personalized plant care advice by retrieving relevant information from a custom-built knowledge base. This project leverages **Amazon Bedrock** Agents with **retrieval-augmented generation (RAG)** to enable seamless Q&A over user-curated content.

---

## 🧠 Problem

Most plant care advice online is fragmented, generalized, or buried in forums and blogs. I wanted to build a tool that could:

- Understand user questions in natural language
- Search through curated plant care documents
- Give precise, helpful responses tailored to specific plants

---

## 💡 Solution

Using **Amazon Bedrock**, I created a chatbot that connects to a custom **knowledge base** built from S3 documents (guides, tips, and care sheets). The bot uses **RAG** with a foundation model (Claude 3 Sonnet) to pull contextually relevant content and generate helpful responses.

---

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
