# Customer-Service-Email-Responder
The Customer Service Email Responder is an n8n workflow that monitors Gmail for new emails, classifies them, and auto-replies to customer support queries. Using Google Gemini with a Pinecone FAQ database, it generates friendly, policy-aware responses signed as Mr. Helpful, Tech Haven Solutions.

#  Customer Service Email Responder (n8n Workflow)

This repository contains an **n8n workflow** that automates **customer service email handling** using:
- **Gmail** (email trigger + reply)
- **Google Gemini API** (AI-powered responses)
- **Pinecone** (FAQ/policy knowledge base)
- **LangChain nodes** (classification + agent)

---

##  Features
-  **Automated Email Monitoring**: Triggers on new incoming emails in Gmail.
-  **Smart Classification**: Classifies emails as *Customer Support* or *Other*.
-  **AI Response Generation**: Uses Google Gemini + Pinecone FAQ database to draft friendly, relevant replies.
-  **Auto Reply**: Sends personalized responses directly back to the customer, signed as *Mr. Helpful from Tech Haven Solutions*.
-  **Fallback Handling**: Non-support emails are ignored safely.

---

##  Workflow Overview
1. **Gmail Trigger** → Detects new incoming emails.
2. **Text Classifier** → Determines if the email is customer support related.
3. **AI Agent (Gemini + Pinecone)** → Drafts an answer using policy/FAQ knowledge base.
4. **Reply to Gmail** → Sends AI-generated reply back to the customer.
5. **No Operation** → Ignores irrelevant emails.

---

##  Requirements
- **n8n** (v1.0+)
- **Gmail API credentials**
- **Google Gemini (PaLM/Gemini) API key**
- **Pinecone API key**

---

##  Usage
1. Import `Customer Service Email Responder.json` into your **n8n instance**.
2. Configure credentials:
   - Gmail OAuth2
   - Google Gemini API
   - Pinecone API
3. Update Pinecone index + namespace (`FAQ`) to point to your support knowledge base.
4. Activate workflow.
5. Test by sending an email → relevant queries get auto-replies, irrelevant ones are ignored.

---

## 📂 Repository Structure

