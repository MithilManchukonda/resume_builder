# AI Resume Builder

This repository is an AI-powered resume builder with a React frontend and a Node.js/Express backend.

## Repository Structure

- `client/` – React/Vite frontend
- `server/` – Express backend with MongoDB and auth services

## Setup

### 1. Install dependencies

From the project root:

```bash
cd client
npm install

cd ../server
npm install
```

### 2. Configure environment variables

Create or update `server/.env` with your MongoDB URI and other settings.

Example:

```dotenv
PORT=5000
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.uy9pwaj.mongodb.net/?appName=Cluster0
JWT_SECRET=your-secret-key
JWT_EXPIRES_IN=7d
CLIENT_URL=http://localhost:5173
GEMINI_API_KEY=your-gemini-api-key
GOOGLE_CLIENT_ID=your-google-client-id
```

### 3. Run the app

In one terminal, start the backend:

```bash
cd server
npm run dev
```

# AI Resume Builder

An intelligent resume builder that combines a React/Vite frontend with a Node.js/Express backend.
This project helps users create, edit, and optimize resumes with AI-powered guidance, ATS scoring, version history, and modern templates.

## Project Idea

The vision behind this project is to simplify resume creation by combining a user-friendly editor with AI-powered feedback.
Users can create a resume, choose a professional layout, and improve their profile using AI review, bullet generation, and job-matching insights.
Authentication ensures resume data is saved securely per user and can be resumed later.

## What I built

- A React front-end for resume creation, live preview, and template selection
- An Express backend with MongoDB persistence and JWT authentication
- Email/password login plus Google sign-in with OAuth
- Resume versioning for saving and restoring prior drafts
- AI integrations for resume review, summary generation, bullet point assistance, and chat
- ATS scoring and job matching to help recruiters find the right keywords in a resume

## Features

- **Authentication** — Email login, registration, Google OAuth, token-based sessions
- **Resume editor** — Personal info, summary, experience, education, skills, certifications
- **Live resume preview** — Visual resume output updates as the user edits
- **Template selection** — Multiple resume templates with different stylings
- **AI assistance** — Automated review, text generation, and resume coaching
- **ATS analysis** — Job description matching, keyword coverage, and improvement suggestions
- **Version control** — Save resume versions and restore older drafts
- **Backend persistence** — User and resume data stored securely in MongoDB

## Architecture

- `client/` — React/Vite frontend with component-based UI and context state management
- `server/` — Express backend with structured controllers, routes, and service layers
- `server/src/config` — configuration for MongoDB, Google OAuth, and AI
- `server/src/models` — Mongoose schemas for users, resumes, versions, and chat history
- `server/src/routes` — API endpoints for auth, resumes, AI, and version history
- `server/src/services` — business logic for authentication, AI calls, and resume persistence

## Built With

- React 19
- Vite
- Express
- MongoDB with Mongoose
- Google OAuth
- Gemini AI via `@google/genai`
- LangChain

## Setup

### 1. Install dependencies

```bash
cd client
npm install

cd ../server
npm install
```

### 2. Configure environment variables

Create `server/.env` with the following values:

```dotenv
PORT=5000
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.uy9pwaj.mongodb.net/?appName=Cluster0
JWT_SECRET=your-secret-key
JWT_EXPIRES_IN=7d
CLIENT_URL=http://localhost:5173
GEMINI_API_KEY=your-gemini-api-key
GOOGLE_CLIENT_ID=your-google-client-id
```

### 3. Run the application

```bash
cd server
npm run dev

cd ../client
npm run dev
```

Then open the browser at the Vite URL.

## Notes

- Do not commit `server/.env` to GitHub.
- Allow your IP in MongoDB Atlas network access.
- Configure Google OAuth credentials for Google login.

## Summary

This project is a complete full-stack resume builder that blends resume editing with AI-powered optimization.
It demonstrates end-to-end development skills in React, Node.js, MongoDB, OAuth, and AI integration.
Use it as a demo of building modern productivity tools with intelligent resume guidance.
