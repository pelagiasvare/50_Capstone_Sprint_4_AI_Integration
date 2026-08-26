# Project 50: Capstone Sprint 4 — AI Integration

## Deliverables
1. **AI service module** — `backend/services/aiService.js` (Project 42)
2. **AI chat endpoints** — `backend/routes/ai.js`, `backend/controllers/aiController.js` (Project 43)
3. **RAG implementation** — `backend/services/ragService.js`, `backend/routes/rag.js` (Project 44)
4. **AI UI components** — `client/src/components/ChatWindow.jsx` (Project 45)
5. **Conversation history** — `backend/services/conversationService.js` + Prisma models (Project 46)

## Integration Flow
```
React ChatWindow ──POST /api/ai/chat──► Express route ──► aiService.generateResponse ──► OpenAI
                                        ▲
React Dashboard ──POST /api/ai/rag──► Express route ──► ragService.answer ──► embeddings + chat
```