# Fix My City — IDEAFORGE26

Tamil Nadu civic reporting app built with React, TypeScript, Vite, Supabase and Leaflet/OpenStreetMap.

## Run locally
1. Install Node.js and run npm install (npm.cmd install in Windows PowerShell).
2. Copy .env.example to .env.local and fill in the Supabase URL and publishable key.
3. Run npm run dev (npm.cmd run dev in Windows PowerShell).
4. Open http://localhost:3000.

## Backend
Supabase SQL migrations and Edge Function source are in supabase/.
See SETUP.txt and AI-SETUP.txt for the original department/AI setup instructions.
The newer pre-submission assessment flow uses priority-before-submit.sql and the assess-draft Edge Function.
Apply ai-priority.sql before priority-before-submit.sql. Add GEMINI_API_KEY in Supabase Edge Function secrets and deploy assess-draft.
SQL repair scripts reflect incremental development: review them before applying to an existing database.
Do not rerun older workflow scripts over newer migrations without checking trigger and policy changes.

## Features
Citizen login, complaints and suggestions, personal/city reports, department review dashboards, in-app notifications, Tamil Nadu map selection, dark mode, and Gemini priority assessment.

## Checks
npm run lint
npm run build

Local environment files, dependencies, build outputs and logs are excluded from Git.
