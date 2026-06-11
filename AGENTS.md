# AI Story Album - Codex Project Rules

## Read First

Before any development work, always read:

1. ./PRD.md
2. ./SYSTEM_DESIGN.md
3. ./TASK_ROADMAP.md

These files are the source of truth.

---

## Project Goal

Build a production-ready WeChat Mini Program:

AI Story Album

User Flow:

Upload Photos
→ Choose Template
→ Generate Album
→ Preview
→ Share
→ Download
→ Pay for Premium Features

---

## Technical Stack

Frontend

* Taro
* React 18
* TypeScript
* Zustand
* React Query

Backend

* NestJS
* Prisma
* MySQL 8

Infrastructure

* Redis
* BullMQ
* Tencent COS
* Docker
* Nginx

Payment

* WeChat Pay V3

AI

* OpenAI
* Gemini

---

## Development Principles

Follow:

* Clean Architecture
* SOLID
* DRY
* KISS

Never:

* Use any type
* Use mock data in production code
* Use pseudo code
* Skip DTO validation
* Skip tests
* Hardcode secrets

---

## Output Requirements

For every task:

1. Explain architecture
2. Update database schema if required
3. Create migration
4. Write backend code
5. Write frontend code
6. Write tests
7. Update documentation

---

## Coding Standards

All modules must contain:

* controller
* service
* dto
* repository
* module

Every database entity must support:

* createdAt
* updatedAt
* deletedAt

Soft delete required.

---

## API Rules

Response format:

Success

{
"code":0,
"message":"success",
"data":{}
}

Error

{
"code":10001,
"message":"error",
"data":null
}

---

## Security

Implement:

* JWT Auth
* Role Guard
* Rate Limit
* Content Review

Roles:

* USER
* VIP
* ADMIN
* SUPER_ADMIN

---

## AI Cost Control

Free User

* 3 albums/day
* 10 AI text generations/day
* 5 AI cover generations/day

Store usage statistics in usage_records.

---

## Final Rule

Always generate production-ready code.

Never sacrifice architecture for speed.
