# GxP AI Governance Assessment Tool

This repository contains a proof‑of‑concept **GxP AI Adoption & Governance Assessment Tool**, built as a single‑file React application.  

The tool walks users through a series of intake questions (I1–I10) and module‑specific checklists (M1–M6) covering the lifecycle of a GxP‑regulated artificial intelligence system — from intake and design through validation, deployment, and continuous monitoring.  It uses local browser storage to save progress and allows users to download or print a report summarizing their compliance posture.

## Running locally

Because this is a raw React component without a build system, you will need to create a minimal React environment to run it.  One option is to scaffold a new Vite or Create‑React‑App project, then replace the `App.jsx` file with the `app.jsx` in this repo.  For example:

```bash
# scaffold a new project (using Vite)
npx create-vite@latest gxp-ai-assessment --template react
cd gxp-ai-assessment
npm install

# replace the default App.jsx with the provided file
mv ../app.jsx src/App.jsx
npm run dev
```

Alternatively, you can embed the contents of `app.jsx` in a CodeSandbox or similar online editor to try it out quickly.

The tool does not send data to any external server — all progress is stored in `localStorage`, and results are computed on the client side.

## About

This assessment was designed as part of a broader effort to align AI adoption with **GAMP 5** guidelines, EU GMP Annex 22, the FDA **Computer Software Assurance** draft guidance, and related regulatory frameworks.  It helps identify key risk areas and ensures that AI systems used in regulated functions meet appropriate requirements for governance, data integrity, validation, and ongoing monitoring.
