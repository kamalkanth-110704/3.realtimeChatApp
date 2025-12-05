
# 🚀 Realtime Chat App

A full-stack **Realtime Chat Application** built using
**Node.js + Express + Socket.IO** for the backend and
**React + Socket.IO Client** for the frontend.

This app supports realtime messaging between users with instant delivery using WebSockets.

---

## 📂 Folder Structure

```
3.realtimeChatApp/
├── backend/       # Express + Socket.IO server
└── frontend/      # React client application
```

---

## ✨ Features

* ⚡ Realtime messaging using Socket.IO
* 👤 User connections & disconnections
* 💬 Room-based or one-to-one chat (depending on implementation)
* 🌐 REST APIs + WebSockets
* 🔧 Easy local development (frontend & backend start separately)
* 📦 Clean folder structure for scaling and deployment

---

## 🛠️ Tech Stack

### **Backend**

* Node.js
* Express
* Socket.IO
* dotenv
* (Optional) MongoDB / JWT (if you add later)

### **Frontend**

* React
* socket.io-client
* React Hooks
* Basic UI components (customizable)

---

# 🚀 Getting Started

Follow the steps below to run the project locally.

---

## 🔹 1. Clone the Repository

```bash
git clone https://github.com/kamalkanth-110704/3.realtimeChatApp.git
cd 3.realtimeChatApp
```

---

## 🔹 2. Run the Backend

```bash
cd backend
npm install
npm start   # or npm run dev if nodemon is used
```

This starts the Socket.IO server (default: **[http://localhost:5000](http://localhost:5000)** unless changed).

If you have an `.env` file, include:

```
PORT=5000
```

---

## 🔹 3. Run the Frontend

```bash
cd ../frontend
npm install
npm start
```

Frontend usually runs on:
👉 **[http://localhost:3000](http://localhost:3000)**

Make sure the frontend connects to the backend socket URL inside your React code (e.g., `socket.io-client("http://localhost:5000")`).

---

# 🔌 Socket.IO Events (Sample)

These are common events used in your chat app (you may adjust based on your code):

### **Client → Server**

* `join` — join a chat
* `send_message` — send a message
* `disconnect` — user leaves

### **Server → Client**

* `receive_message`
* `user_joined`
* `user_left`

---

# 🧪 Example Message Format

```json
{
  "roomId": "123",
  "sender": "User1",
  "message": "Hello!",
  "timestamp": 1700000000
}
```

---

# 📦 Build for Production

### Frontend

```bash
cd frontend
npm run build
```

### Backend

Deploy using Node/PM2/Vercel/Render etc.

---

# 🐞 Troubleshooting

| Issue                             | Fix                                              |
| --------------------------------- | ------------------------------------------------ |
| Frontend can't connect to backend | Check Socket.IO URL, CORS settings               |
| Messages not appearing            | Ensure event names match on both sides           |
| Server crashes                    | Check for missing packages or wrong import paths |

---

# 🤝 Contributing

Feel free to fork the repo, improve features, and create PRs.

---

# 📜 License

This project is open-source. You can add your preferred license.

---

# 🙌 Author

**Kamal Kanth**
Realtime Chat App Developer

---

