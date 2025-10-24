# Overview
Orange(BTC) Standard가 진행되면서 관심있는 사람들의 Citadel 유입이 늘어가고 있다.
오래 공부한 OG들의 답변 피로도가 올라가고 있고 애매하게 아는 사람들의 잘못된 답변이 생길 우려가 있다.
때문에 Citadel에서 정리되어 검수된 정보를 바탕으로 AI에게 오스트리안학파 Bitmaxi의 관점으로 답변을 주는 Agetic Bot을 개발하고자 한다.

# Requirements
## FR-01. 구성된 WIKI를 바탕으로 정확한 지식정보를 RAG로 활용하여 응답한다.
## FR-02. ...

# Architecture
Discord Slash Cmd
        │
        ▼
 Command Router ──▶ Rate Limiter
        │
        ▼
   Agent Loop ── Plan → Select Tool(Citadel WIKI DataSource) → Act → Observe → Iterate (k≤3) -> Planning이 필요 없을지도...
        │
        │
        └─▶ Output Guard → Formatter → Discord Reply

## RAG Pipeline (WIKI) - Phase2
  1) Query Rewrite
  2) Dense Retrieval (Vector DB)
  3) Re-Rank (Cross-Encoder, 선택)
  4) Grounded Answer Synthesis

# Tech.
## Bot
- python 3.11
## Agent API
- FastAPI
- DB : supabase serverless
- llm : grok-4-fast(openrouter)
## Agent Runtime
- 흐으으음 뭘쓰지...
- 

