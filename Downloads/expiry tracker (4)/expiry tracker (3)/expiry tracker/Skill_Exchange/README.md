# Skill Exchange

Skill Exchange is a lightweight web app scaffold for connecting mentors and mentees. This README documents the intended folder layout and how to run the app locally.

Overview

- Minimal Express static server that serves the frontend from `public/`.
- Optional WebSocket/Socket.IO support can be added in `server.js` for real-time messaging.

Folder structure

Skill_Exchange/
├─ server.js                 # (optional) Express server entrypoint
├─ package.json              # (optional) npm manifest for server and build scripts
└─ public/                   # Static frontend files served by the server
   ├─ index.html             # Landing / home page
   ├─ login.html             # Login page
   ├─ signup.html            # Signup / register page
   ├─ mentor-dashboard.html  # Mentor dashboard view
   ├─ mentee-dashboard.html  # Mentee dashboard view
   ├─ messages.html          # Messaging / chat UI
   └─ admin-dashboard.html   # Admin dashboard

How to use

1. Place this folder inside your workspace or clone the original repository.

2. If you plan to run the server, ensure `server.js` and `package.json` exist, then run:

   npm install
   npm start

3. If there is no server, open `public/index.html` directly in a browser or serve the `public/` directory using any static server.

Notes

- This README only documents the folder layout and how the project is expected to be run; no other files were modified.
- For a reference implementation, see: https://github.com/23wh1a0513/Skill-Exchange

License

MIT (or choose your preferred license)

