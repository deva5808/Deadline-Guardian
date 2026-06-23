# Deadline Guardian

Deadline Guardian is a functional solution for **Problem Statement 1: The Last-Minute Life Saver**.
It is an AI-powered productivity companion that helps users prioritize urgent work, build rescue plans,
track habits, capture tasks by voice, and export calendar blocks before deadlines are missed.

## Live Demo

[Deadline Guardian deployed app](https://deadline-guardian-306175130476.asia-southeast1.run.app)

## Problem Statement

Students, professionals, and entrepreneurs frequently miss deadlines, assignments, meetings, bill payments,
interviews, and other important commitments. Existing productivity tools often depend on passive reminders
that are easy to ignore.

Deadline Guardian solves this by helping users take action before deadlines are missed. It prioritizes tasks,
builds rescue plans, supports habit tracking, and helps users move planned work into a calendar.

## Key Features

- Intelligent task prioritization with urgency, effort, and blocker scoring.
- Gemini-powered action plans using an API key from Google AI Studio.
- Local fallback planner so the demo remains usable without network access.
- Voice-enabled task capture through the browser Speech Recognition API.
- Goal and habit tracking with daily streaks.
- Calendar export as `.ics` for Google Calendar or other calendar tools.
- Submission-friendly documentation for BlockseBlock hackathon requirements.

## Google Technologies Used

- Google AI Studio for Gemini API key creation and deployment workflow.
- Gemini API model endpoint: `gemini-3.5-flash:generateContent`.
- Google Cloud Run deployment URL when published through Google AI Studio Build Mode.
- Google Calendar compatible `.ics` export.

## How It Works

1. The user adds a task with deadline, effort, and optional context.
2. The app calculates a risk score using time remaining, effort, and blockers.
3. The highest-risk tasks are pushed to the top of the priority queue.
4. Gemini generates a concise rescue plan when an API key is provided.
5. If Gemini is unavailable, the built-in local planner still creates a useful action plan.
6. Users can export active tasks as calendar blocks using the `.ics` format.

## Run Locally

Open `index.html` in a browser.

For live Gemini recommendations:

1. Go to [Google AI Studio](https://aistudio.google.com/).
2. Create or copy a Gemini API key.
3. Open the app, go to **Assistant**, paste the key, and click **Save Key Locally**.

The key is stored only in your browser local storage for demo purposes.

## Deploy with Google AI Studio

The hackathon requires a deployed application link using Google AI Studio. The official Google doc says
AI Studio Build Mode can publish full-stack apps and provides a Cloud Run URL after publishing.

Suggested flow:

1. Open Google AI Studio Build Mode.
2. Create a new app named `Deadline Guardian`.
3. Upload or recreate these files: `index.html`, `styles.css`, and `app.js`.
4. Verify the app runs and Gemini calls work with your API key.
5. Click **Publish**, then **Get Started**, then **Publish App**.
6. Copy the generated Cloud Run URL as your deployed application link.

Reference: [Deploying from Google AI Studio](https://ai.google.dev/gemini-api/docs/aistudio-deploying).

## Submission Checklist

- Deployed Application Link: Google AI Studio / Cloud Run URL.
- GitHub Repository Link: upload this project folder to GitHub.
- Project Description Google Doc: use `PROJECT_DESCRIPTION.md` as the source content.
- Problem Statement Selected: Problem Statement 1, The Last-Minute Life Saver.

## Evaluation Matrix Alignment

- **Problem Solving and Impact:** focuses on helping users complete tasks before deadlines.
- **Agentic Depth:** ranks tasks, adapts plans, and recommends next actions.
- **Innovation and Creativity:** combines task triage, AI planning, habit momentum, voice capture, and calendar export.
- **Google Technologies:** uses Google AI Studio, Gemini API, Cloud Run deployment, and calendar-compatible export.
- **Product Experience:** clean dashboard with Mission, Tasks, Habits, and Assistant views.
- **Technical Implementation:** lightweight browser app with persistence, AI integration, and graceful fallback behavior.
- **Completeness and Usability:** deployed, documented, and usable with or without a Gemini API key.

## Project Structure

```text
last-minute-life-saver/
  index.html
  styles.css
  app.js
  README.md
  PROJECT_DESCRIPTION.md
  SUBMISSION_STEPS.md
```
