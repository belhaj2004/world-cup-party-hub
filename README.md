# World Cup Party Hub

A simple interactive World Cup watch-party website where friends can join, submit match predictions, play trivia, mark bingo squares, use the crowd meter, and view a live leaderboard.

## Live Site

https://belhaj2004.github.io/world-cup-party-hub/

## Features

- Score prediction wall
- Random World Cup trivia questions on login
- Bingo card for match moments
- Crowd-O-Meter
- Live leaderboard
- Mobile-friendly design
- GitHub Pages deployment
- Firebase/Firestore support for shared live data

## How to Update the Website

1. Download or edit the latest `index.html` file.
2. Go to the GitHub repository:
   
   https://github.com/belhaj2004/world-cup-party-hub

3. Replace the existing `index.html` file.
4. Commit the change to the `main` branch.
5. Wait about 30-60 seconds for GitHub Pages to redeploy.
6. Refresh the live website.

## Firebase Setup

This project uses Firebase Firestore to store shared data such as predictions, player scores, crowd meter totals, and leaderboard information.

To use it:

1. Create a Firebase project.
2. Register a Web App.
3. Copy the Firebase configuration into `index.html`.
4. Enable Firestore Database.
5. For testing, use Firestore test rules.

Example test rules:

```js
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

Note: These rules are only recommended for a temporary public party/game setup. Do not use open rules for sensitive or private data.

## GitHub Pages Deployment

GitHub Pages should be set to:

- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`

The main website file must be named exactly:

```text
index.html
```

## Project Purpose

This was built as a quick, fun World Cup prediction and party hub for friends, coworkers, or public groups to share their match predictions and interact during games.

## Author

Created by Adib.
