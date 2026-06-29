# RobloxWatcher Server

Tiny Node.js proxy for fetching Roblox presence info & join links.  
Required backend for the [RobloxWatcher Tampermonkey userscript](https://greasyfork.org/en/scripts/548192).

[👉 **Install the RobloxWatcher Userscript on GreasyFork**](https://greasyfork.org/en/scripts/548192)


---

## 🚀 Setup

### 1. Clone and install
```bash
git clone https://github.com/gaston1799/RobloxWatcher.git
cd RobloxWatcher
npm install
```

### 2. Configure environment
Copy the example file:
```bash
cp .env.example .env
```

Then edit `.env` and paste your **.ROBLOSECURITY** cookie (see below for how to retrieve it):

```env
ROBLOSECURITY=your_cookie_here
PORT=3000
```

⚠️ Never commit `.env` with your real cookie. It’s ignored in `.gitignore`.

---

## 🔑 Retrieving your `.ROBLOSECURITY` cookie

1. Install the [Cookie Editor extension](https://chromewebstore.google.com/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm).
2. Go to [https://www.roblox.com](https://www.roblox.com) and log in.
3. Click the Cookie Editor extension icon.
4. Find the cookie named **`.ROBLOSECURITY`**.
5. Copy its **value** (long string starting with `_|WARNING:...`).
6. Paste it into your `.env` file:
   ```env
   ROBLOSECURITY=_|WARNING:...yourlongcookiehere...
   ```

---

## 3. Run the server
```bash
npm run dev
```

Default: [http://localhost:3000](http://localhost:3000)

---

## 🛠 Endpoints

- `GET /health`  
  → `{ ok: true }`

- `GET /presence-raw?userIds=123,456`  
  → Raw Roblox API presence payload

- `GET /presence-users?userIds=123,456`  
  → Presence + last seen in game

- `GET /server-link?userId=123`  
  → Join link if the user is in a public game

- `GET /join-by-follow?userId=123`  
  → Fallback link using Roblox’s follow system

---

## 🔒 Security

- Keep your `.ROBLOSECURITY` **private**.
- Do not deploy this server publicly unless you trust the environment.
- Intended for local use with the RobloxWatcher userscript.

---

## ✅ Next Steps

- Install the RobloxWatcher userscript in Tampermonkey.
- Point it at `http://localhost:3000`.

---
