# AI Story Album System Design

# Architecture

Frontend

Taro + React + TypeScript

Backend

NestJS + Prisma

Database

MySQL 8

Storage

Tencent COS

Cache

Redis

Queue

BullMQ

Deployment

Docker

Nginx

---

# Core Modules

## Auth

Functions

* WeChat Login
* JWT

## User

Functions

* Profile
* Membership

## Upload

Functions

* COS Upload Token
* Image Management

## Album

Functions

* Create Album
* Generate Album
* Preview Album

## Template

Functions

* Template Management

## Payment

Functions

* WeChat Pay V3
* Refund

## Share

Functions

* Share Tracking

## AI

Functions

* Image Analysis
* Story Generation
* Cover Generation

---

# Database Entities

User

Album

AlbumImage

AlbumPage

Template

Order

Payment

VipRecord

ShareRecord

AiTask

UsageRecord

---

# Album Generation Engine

Input

* Images
* Template

Output

AlbumPage[]

Supported Layouts

* cover
* single
* double
* triple
* grid
* timeline
* ending

Generation must be dynamic.

No hardcoded page count.

---

# AI Architecture

Provider Pattern

AiProvider

OpenAIProvider

GeminiProvider

Future

ClaudeProvider

QwenProvider

Business layer must not depend on vendor implementation.

---

# Queue Tasks

BullMQ

Jobs

* AI Analysis
* PDF Export
* Cover Generation
* Story Generation
* Poster Generation

---

# Security

JWT

Role Guard

Rate Limit

Content Moderation

Audit Log

---

# Monitoring

Health Check

/health

Metrics

Prometheus

Visualization

Grafana

---

# CI/CD

GitHub Actions

Pipeline

Lint

Test

Build

Docker Build

Deploy

---

# Testing

Jest

Coverage > 80%

Required:

* Auth
* Album
* Payment
* AI
