# English Grammar Content Manager

A sleek, self-hosted web-based administration panel to view, create, update, and delete English grammar JSON content. It allows management of both levels (rosters and ordering) and units (detailed usages, signal words, common mistakes, and quizzes).

---

## 🛠️ Tech Stack & Design

- **Backend**: Node.js & Express API for secure local JSON file operations.
- **Frontend**: Single Page Application (SPA) built using Semantic HTML5, Vanilla JS, and custom CSS.
- **Aesthetics**: Premium responsive dark-mode layout featuring modern typography, dynamic hover interactions, glassmorphic card surfaces, drag-and-drop animations, and instant action toasts.

---

## 🚀 How to Run the Admin Panel

Follow these simple steps to get the content manager running locally:

### 1. Install Dependencies
Navigate to the `admin/` directory and install the necessary npm packages (`express` and `cors`):
```bash
cd admin
npm install
```

### 2. Start the Server
Run the local Express server:
```bash
npm start
```

### 3. Open the App
Once started, open your web browser and navigate to:
```
http://localhost:3131
```

---

## 📂 Project Structure

```
english-grammar/
├── admin/                 # Admin Panel Web App (Git Ignored)
│   ├── package.json
│   ├── server.js          # REST API & Static File Server
│   ├── index.html         # Main Web Interface
│   ├── app.js             # Frontend Logic
│   └── style.css          # Styling & Animations
├── levels/                # JSON Stubs/Syllabus for Levels
│   ├── a1.json
│   ├── a2.json
│   └── ...
├── units/                 # JSON Data for Detailed Units
│   ├── a1_nouns.json
│   ├── a1_adjectives.json
│   └── ...
└── .gitignore             # Configured to ignore the admin tools
```

---

## 📝 Key Features

- **🏆 Level Roster Management**:
  - Drag and drop stubs to instantly reorder units inside levels.
  - Add existing units to a level list using a smart selector (only shows units not already in the level).
  - Remove stubs safely from a level without deleting the original unit file.

- **📄 Full Unit CRUD Editor**:
  - Update positive/negative/question forms.
  - Create and manage usage categories, adding infinite sample sentence lists.
  - Tag signal words using an interactive tag manager.
  - Document common mistakes with incorrect/correct styling and custom explanations.
  - Add and structure multiple-choice quizzes with selectable correct-answer options.

- **💾 File-Sync & Safety**:
  - Save buttons write directly to the local filesystem.
  - Double-guards against losing unsaved changes (warns when navigating away from dirty edits).
  - Copy JSON output preview directly with one click.
