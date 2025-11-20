#  Image Generation Agent with MCP + Cost Approval

This project is an **Image Generation Agent** built using **Google ADK** and the **Model Context Protocol (MCP)**.

It allows controlled image generation by adding a **cost approval workflow** for bulk image requests.

---

## 🚀 Features

✅ Auto-generates images for small requests  
✅ Pauses and asks for approval for bulk requests  
✅ Uses MCP public image generation servers  
✅ Built using Google ADK Agent framework  

---

## 🧠 How the Approval Logic Works

| Number of Images | Behaviour |
|------------------|-----------|
| 1 image           | Auto-approved ✅ |
| 2–5 images        | Auto-approved ✅ |
| More than 5       | Requires manual approval ⏸️ |

For bulk requests, the agent pauses and uses:

- `ToolContext.request_confirmation()`
- Resumes only after approval is received.

