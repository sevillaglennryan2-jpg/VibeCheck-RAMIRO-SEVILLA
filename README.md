# VibeCheck 411LS

### Prerequisites
- Node.js installed on your system
- npm (Node Package Manager)

### Run Steps

1. **Install Backend Dependencies**
   ```bash
   cd backend
   npm install
   ```

2. **Start the Backend Server**
   ```bash
   node index.js
   ```
   - The server will start on `http://localhost:3000`
   - You should see: `VibeCheck API running at http://localhost:3000`

3. **Open the Frontend**
   - Navigate to the `frontend` folder
   - Open `index.html` in your web browser
   - You should see the VibeCheck interface with animated buttons

4. **Interact with the Application**
   - Click buttons to fetch data from the API
   - Check the output section for responses

## API Endpoints

### GET /api/fortune
Returns a random fortune message.

**Response:**
```json
{
  "fortune": "You will debug it in 5 minutes... after 55 minutes of panic."
}
```

---

### GET /api/joke
Returns a random joke.

**Response:**
```json
{
  "joke": "Why did the developer go broke? Because they used up all their cache."
}
```

---

### GET /api/vibe?mood={mood}
Returns a mood-specific message and emoji.

**Parameters:**
- `mood` (required): `happy`, `tired`, or `stressed`

**Response Example (mood=happy):**
```json
{
  "mood": "happy",
  "emoji": "😄",
  "message": "Keep going - you're shipping greatness!"
}
```

**Available Moods:**
- `happy` → 😄 "Keep going - you're shipping greatness!"
- `tired` → 🥱 "Hydrate. Stretch. Then commit."
- `stressed` → 😵‍💫 "Breathe. One bug at a time."

---

### POST /api/smash
Increments the smash counter and returns the updated value.

**Response:**
```json
{
  "smashes": 1
}
```

---

### GET /api/smashes
Returns the current smash counter value.

**Response:**
```json
{
  "smashes": 5
}
```

---

### GET /api/secret?code={code}
Returns a secret message if the correct code is provided.

**Parameters:**
- `code` (required): `411L`

**Success Response (code=411L):**
```json
{
  "message": "🎉 Secret unlocked: +10 luck on your next merge!"
}
```

**Error Response (wrong code):**
```json
{
  "message": "Nope 😄 Try code=411L"
}
```




