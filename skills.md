# CatSU Sepak Takraw Checklist Project Skill

## Project Focus

This project is a simple CatSU Sepak Takraw Requirements Checklist web app. Focus only on improving, fixing, and maintaining this project. Do not introduce unnecessary features, frameworks, dependencies, or architecture changes.

## Core Requirement

Data added by the administrator on one device must remain saved and, after the shared data is published/deployed, must be visible when the same Vercel link is opened on another device.

The app must NOT use:

* Supabase
* Firebase
* MySQL
* PostgreSQL
* MongoDB
* Any online database
* Backend server
* Authentication/login
* External data-storage APIs

## Data Architecture

Keep `localStorage` for local and offline data.

Use a simple shared data file such as `shared-data.json` as the source of data that gets included in the deployed Vercel application.

Flow:

Vercel → shared-data.json → localStorage → user device

The goal is that data added by the administrator can be published into the deployed app so other devices opening the same URL can see the same data.

## Existing Features

Do not remove or redesign:

* Yellow and black UI
* Player management
* Men/Women classification
* Requirements management
* Checklist functionality
* Responsive design
* PWA functionality
* Offline functionality
* Existing localStorage behavior

## Data Persistence

Always preserve existing data when modifying the application.

Never automatically clear localStorage.

When shared data is loaded, avoid overwriting newer local data without confirmation.

## Shared Data

The app should support exporting current data into `shared-data.json`.

The administrator can then replace the project's shared data file and redeploy the application.

Other devices should load the latest deployed shared data when opening the app.

## Development Rules

Before changing code:

1. Inspect the existing implementation.
2. Reuse the existing structure.
3. Make the smallest change necessary.
4. Do not rewrite working features.
5. Do not add unnecessary dependencies.
6. Do not change the UI unless explicitly requested.
7. Test existing functionality after every major change.

## Priority

Always prioritize:

1. Data persistence
2. Cross-device shared data
3. Offline functionality
4. Existing features
5. Simple implementation
6. Minimal code changes

Do not spend time on unrelated improvements.

## Communication

When working on this project, focus only on the requested task. Keep explanations short and practical. Do not suggest unrelated technologies or features unless they are necessary to solve the current problem.
