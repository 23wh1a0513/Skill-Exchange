# Skill Exchange

Skill Exchange

Skill Exchange is a small web app scaffold used to connect mentors and mentees. This README focuses on a clear, visual project structure and quick usage notes so the repository looks like the example image.

Project Structure

The layout below mirrors the screenshot/design you shared:

Skill_Exchange/
├─ server.js    # Main Express + WebSocket server
├─ package.json
├─ README.md
└─ public/
   ├─ index.html               # Landing page
   ├─ login.html
   ├─ signup.html
   ├─ mentor-dashboard.html
   ├─ mentee-dashboard.html
   ├─ messages.html
   └─ admin-dashboard.html

How to run (quick)

- If you have `server.js` and `package.json` present, run:

```bash
cd Skill_Exchange
npm install
npm start
```

- If there is no server, you can open `public/index.html` in a browser or serve it with any static server (e.g., `npx serve public`).

Notes

- This README only updates documentation and formatting; it does not change any project code or add files.
- For the original reference repo see: https://github.com/23wh1a0513/Skill-Exchange

License

MIT

