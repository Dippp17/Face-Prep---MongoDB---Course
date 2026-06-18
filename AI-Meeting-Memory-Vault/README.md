# AI Meeting Memory Vault

An AI-powered backend application that stores meeting transcripts, generates intelligent summaries, enables meeting search, provides analytics, and allows users to interact with historical meeting data using Google Gemini AI.

---

## Overview

AI Meeting Memory Vault is a backend system designed to preserve organizational knowledge by storing meeting transcripts and transforming them into searchable, AI-enhanced records.

The application combines MongoDB, Express.js, and Google Gemini AI to automate meeting documentation and improve information retrieval.

---

## Features

### Meeting Management

* Create Meeting
* Get All Meetings
* Get Meeting By ID
* Update Meeting
* Delete Meeting

### AI Features

* AI-generated meeting summaries
* Action item extraction
* Decision extraction
* AI-powered chat with meeting history

### Search

* Full-text search using MongoDB Text Indexing
* Search meetings by keywords

### Analytics

* Dashboard statistics
* Meeting count analytics
* Action item statistics
* Decision statistics

### File Upload

* Upload transcript files (.txt)
* Automatic transcript processing
* Summary generation after upload

### Additional Features

* Pagination
* Filtering
* Swagger API Documentation

---

## Tech Stack

### Backend

* Node.js
* Express.js

### Database

* MongoDB
* Mongoose

### Artificial Intelligence

* Google Gemini AI

### File Handling

* Multer

### API Testing

* Postman

### API Documentation

* Swagger UI
* Swagger JSDoc

---

## Project Structure

```text
AImeetingMemoryVault
│
├── server.js
├── package.json
├── .env
├── seed.js
│
└── src
    │
    ├── app.js
    │
    ├── config
    │   └── db.js
    │
    ├── controllers
    │   └── meetingController.js
    │
    ├── middleware
    │   └── upload.js
    │
    ├── models
    │   └── Meeting.js
    │
    ├── routes
    │   └── meetingRoutes.js
    │
    ├── services
    │   ├── aiSummaryService.js
    │   ├── analyticsService.js
    │   └── chatService.js
    │
    └── swagger
        └── swagger.js
```

---

## Installation

### Clone Repository

```bash
git clone <repository-url>
cd AImeetingMemoryVault
```

### Install Dependencies

```bash
npm install
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
PORT=7000

MONGO_URI=mongodb://127.0.0.1:27017/ai_meeting_vault

GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

---

## Running the Application

### Development Mode

```bash
npm run dev
```

### Production Mode

```bash
npm start
```

---

## Seed Sample Data

Populate the database with sample meetings.

```bash
npm run seed
```

---

## API Endpoints

### Home

```http
GET /
```

---

### Create Meeting

```http
POST /api/meetings
```

---

### Get All Meetings

```http
GET /api/meetings
```

---

### Get Meeting By ID

```http
GET /api/meetings/:id
```

---

### Update Meeting

```http
PUT /api/meetings/:id
```

---

### Delete Meeting

```http
DELETE /api/meetings/:id
```

---

### Search Meetings

```http
GET /api/meetings/search?q=mongodb
```

---

### Dashboard Analytics

```http
GET /api/meetings/dashboard
```

---

### Upload Transcript

```http
POST /api/meetings/upload
```

---

### Generate AI Summary

```http
POST /api/meetings/:id/summary
```

---

### AI Chat

```http
POST /api/meetings/chat
```

Example Request:

```json
{
  "question": "What decisions were made about MongoDB?"
}
```

---

## Swagger Documentation

Start the server and open:

```text
http://localhost:7000/api-docs
```

Swagger provides interactive API documentation for all endpoints.

---

## Database Schema

### Meeting

```javascript
{
  title: String,
  transcript: String,

  summary: {
    overview: String,
    actionItems: [String],
    decisions: [String]
  },

  tags: [String],
  participants: [String],

  meetingDate: Date,

  createdAt: Date,
  updatedAt: Date
}
```

---

## Workflow

```text
Upload Transcript
        ↓
Store Transcript
        ↓
Generate AI Summary
        ↓
Store Summary
        ↓
Search Meetings
        ↓
View Analytics
        ↓
Chat With Meeting History
```

---

## Learning Outcomes

* REST API Development
* Express.js Routing
* MongoDB CRUD Operations
* Mongoose Data Modeling
* File Upload Handling
* AI Integration using Gemini
* MongoDB Text Search
* Aggregation Pipelines
* API Documentation with Swagger
* Postman Testing
* Backend Project Architecture

---

## Future Enhancements

* Authentication & Authorization
* PDF Report Generation
* Semantic Search
* Docker Deployment
* Unit Testing
* Cloud Deployment
* Advanced Analytics

---
