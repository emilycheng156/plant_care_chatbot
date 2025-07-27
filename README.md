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

<img width="822" height="427" alt="Screenshot 2025-07-27 at 4 33 33 PM" src="https://github.com/user-attachments/assets/2a82a728-983a-416f-bf2b-b1d1153fa5ee" />

- 📄 **Amazon S3** holds structured plant care docs (PDFs, guides, etc.)
- 🧠 **Titan Text Embeddings v2** converts documents into semantic vectors
- 🔍 **Amazon OpenSearch Serverless** stores and retrieves embeddings
- 🤖 **Amazon Bedrock Agent** (LLaMA 3.3 70B) answers questions using retrieved content
This RAG architecture ensures that every answer is grounded in reliable source material — no hallucination, no guesswork.


---
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

### 📝 What I Learned

Through this project, I gained hands-on experience with building a Retrieval-Augmented Generation (RAG) chatbot using Amazon Bedrock and related AWS services. I learned how to:

- Set up a **Knowledge Base in Amazon Bedrock**, connecting it to documents stored in Amazon S3
- Use **Titan Text Embeddings v2** to convert text into semantic vector representations
- Configure and deploy **Amazon OpenSearch Serverless** as a vector store for fast, meaningful retrieval
- Choose and apply a suitable **foundation model** (LLaMA 3.3 70B Instruct) for generating responses
- Understand the difference between **on-demand vs. provisioned inference**, and how to troubleshoot model invocation issues
- Enable **retrieval-augmented generation** to ground responses in specific, trusted documents and reduce hallucination
- Improve response quality through **prompt engineering** and plan for **fine-tuning** to better handle edge cases

Overall, this project gave me a practical understanding of how to integrate multiple AWS services to build a scalable, domain-specific chatbot.

### 🔄 Next Steps

To improve the chatbot’s performance even further, the next phase will focus on:
- **Prompt engineering** to guide tone, completeness, and contextual accuracy.
- **Fine-tuning** on more targeted plant care data to handle edge cases like pest issues or seasonal needs.
- Exploring **multi-turn conversation handling** so the chatbot can follow up or clarify when users ask complex or vague questions.



## 📎 Related Links

- 🔁 [What is Retrieval-Augmented Generation (RAG)?](https://www.pinecone.io/learn/retrieval-augmented-generation/)
- 🤖 [Amazon Bedrock Overview](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html)
- 🧠 [Meta’s LLaMA Models](https://ai.meta.com/llama/)
- 📊 [Titan Text Embeddings v2 (AWS)](https://docs.aws.amazon.com/bedrock/latest/userguide/model-access.html#foundation-models-titan)
- 🔍 [Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless.html)
