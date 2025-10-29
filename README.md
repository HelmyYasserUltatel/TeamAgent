# Team Work Reporter AI — Minimal Next.js Project

## What this contains
- A minimal Next.js app with:
  - `/update` page for team members to submit updates
  - `/dashboard` page for managers to view updates and generate AI summary
  - API routes: `/api/update` (extracts JIRA IDs and fetches issue basic info) and `/api/summary` (generates an AI paragraph summary)
  - Firebase integration (Firestore) for realtime storage

## How to use
1. Install dependencies:
   ```bash
   npm install
   ```
2. Configure environment variables. Copy `.env.example` to `.env.local` and fill values.
3. Run locally:
   ```bash
   npm run dev
   ```
4. Deploy to Vercel (connect your GitHub repo) and add the same environment variables in Vercel.

## Notes
- The `/api/summary` endpoint will try to use Hugging Face inference API if you provide `HUGGINGFACE_API_KEY`.
  If not set, it uses a templated summary generator that creates an English paragraph.
- You must provide Jira credentials (email + API token) with read permissions.
- This repo is a **minimal starter** — feel free to enhance styling (Tailwind), authentication (Firebase Auth),
  and error handling.

## Environment (.env.local)
See `.env.example` for required variables.

