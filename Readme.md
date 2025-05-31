# Smart Autocorrect System using Trie and Edit Distance

## Made by :-
**Allan Santosh Joseph**

---

## 📌 Project Objective

To build a smart autocorrect engine using:
- Trie data structure for efficient word storage and lookup.
- Edit Distance (Levenshtein Distance) for typo correction.
- Priority Queue to rank correction suggestions.

---

## 🎯 Features
- Loads a dictionary of valid English words.
- Accepts user input and checks spelling.
- If incorrect, suggests up to 10 close matches based on:
  - Insertions
  - Deletions
  - Substitutions
  - Transpositions
- Suggestions limited to edit distance ≤ 2.
- Web interface for real-time autocorrection suggestions.

---

## 🧠 Learning Outcomes

- Implemented and optimized a **Trie**.
- Understood and applied **Edit Distance algorithms**.
- Used **priority queues** for ranking results.
- learned how to deploy the backend cpp code using **Render**.
- **Express.js** and **node.js** for interconnecting frontend and backend.

---

## 📂 Project Structure

SmartAutocorrect/
│
├── Backend/
│ ├── build.sh # Script to compile trie.cpp
│ ├── dictionary.txt # Word list used by Trie
│ ├── package.json # Node.js dependencies
│ ├── package-lock.json # Auto-generated dependency lock file
│ ├── server.js # Express server
│ ├── trie.cpp # Core C++ autocorrect logic
│ └── trie.exe # Compiled C++ binary (Windows)
│
├── Frontend/
│ ├── dictionary.txt # Optional local reference
│ ├── index.html # Web UI for user input
│ └── Readme.md # Project documentation (this file)
│
├── node_modules/ # Installed npm modules (auto-generated)

---

## 🔧 How to Run the Program

### 1. Compile the C++ code
Ensure you have g++ installed.
```bash```
g++ trie.cpp -o trie.exe

### 2. Start the Node.js server
Ensure Node.js is installed. Then:

npm install express cors
node server.js
### 3. Open the Web Interface
Visit:

http://localhost:3000
Type in the input field to receive live spelling suggestions.

**⚙️ How It Works**

1. Dictionary Building:

Words from dictionary.txt are inserted into a Trie.

2. Input Handling:

User input is received from the frontend.

3. Error Detection & Suggestions:

If word is not found, suggestions are generated using Edit Distance ≤ 2.

4. Suggestion Ranking:

Suggestions are ranked using a max-heap based on closeness (min edit distance).

5. Output:

Top suggestions are returned to the frontend for display.

### 📝 Assumptions Made
All dictionary words are lowercase.

Maximum edit distance for suggestions is 2.

A command-line executable (trie.exe) is called from the server.