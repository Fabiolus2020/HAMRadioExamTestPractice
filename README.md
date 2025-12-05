# 📡 HAM Exam Trainer (Canada) — Bilingual Study App

A free, offline-ready HTML tool to help you practice for the **Canadian Amateur Radio Basic and Advanced exams**.

- 🇨🇦 Based on the official ISED question banks
- 🇬🇧🇫🇷 Fully bilingual interface (English & French)
- 📱 Mobile-friendly (PWA-ready) single-page app
- 🧠 Multiple study modes, including official exam structures
- 🧾 Optional CSV question bank with explanations

Created by **Fabien Clermont**.  
Licensed under **CC BY-NC-SA 4.0** (non-commercial, attribution, share-alike).

---

## ✨ Features

### 📚 Supports Both Official ISED Question Banks

The app can load the **official delimited TXT files** published by ISED:

- `amat_basic_quest_delim2025.txt` (Basic)
- `amat_adv_quest_delim2025.txt` (Advanced)

You can either:

- Load them **directly from GitHub** using the built-in buttons, or  
- Download them yourself and use **“Choose a file”** to load a local copy.

When an official bank is loaded, the app:

- Follows the **real exam category distributions**:
  - Basic: 100 questions (8 categories, fixed counts)
  - Advanced: 50 questions (7 categories, fixed counts)
- Displays **category performance statistics** and **weak-area detection**.

> 🔎 The official ISED banks do **not** contain explanations — they are pure questions and answers.

---

## 🧾 Optional CSV Question Bank With Explanations

In addition to the official TXT banks, the app supports a **custom CSV format** that allows you (or any user) to add:

- Detailed **explanations** for each question  
- **Memory tricks** and learning tips  
- HTML-safe formatted text (for use inside the app)  
- Your own improvements or clarifications

A sample CSV is provided in the repository, for example:

- `BankQuestionJuly2025.csv`

You can:

1. Download the CSV file from GitHub.
2. Open it in Excel, Google Sheets, or LibreOffice.
3. Edit or add explanations, memory aids, or improved wording.
4. Save it as CSV and load it using the app’s **“Choose a file (local)”** button.

When a compatible CSV is loaded:

- The app will show an **Explanation** section after you press **“Check Answer”**.
- This explanation is pulled directly from the CSV’s `explanation` column.
- This is ideal for students who want to understand *why* an answer is correct, not just which letter to choose.

> 💡 Note: The official government TXT banks do not include explanations.  
> The CSV explanation bank is a **user-created enhancement**. I (Fabien) am actively working on improving and expanding explanations, but end users are free to customize their own CSV for personal study.

### 📁 Recommended CSV Structure

A typical row in the CSV looks like this (columns may vary slightly):

- `question` — Question text  
- `optionA`, `optionB`, `optionC`, `optionD` — Answer choices  
- `correctOption` — Which answer is correct (`A`, `B`, `C`, or `D`)  
- `explanation` — HTML-safe explanation text (shown after checking the answer)  
- `BankQuestionID` — Optional ID that matches the official bank (e.g. `B-001-001-002`)

The app is flexible, but following this structure is recommended for best results.

---

## 🧪 Study & Exam Modes

The app supports several modes to match different study styles:

### 🎯 Exam Mode (Official Structure)

- **Basic:** 100 questions chosen to match the official category distribution.
- **Advanced:** 50 questions chosen to match the official category distribution.
- Shows:
  - Final score and percentage
  - **Pass / Fail / Pass with Honours**
  - Category breakdown (e.g. Regulations, Operating, Electronics…)
  - **Weak-area detection** with “Practice only this category” buttons
  - “Retake only wrong questions” button

### 🔄 Random Mode

- Picks random questions from the loaded bank.
- Good for general practice and quick sessions.

### ♻️ No-repeat Mode

- Goes through all questions **without repeats** until the set is exhausted.
- Ideal for full-bank coverage.

### 🧩 Category Training (By Topic)

- Lets you pick one or more categories to focus on (e.g. only “Propagation”, only “Antennas”).
- Great for eliminating weak points.

### 🔁 Retake Wrong Questions

- After an exam, you can launch a session containing **only the questions you answered incorrectly**.
- The app builds a fresh question sequence from your mistakes.

---

## 📊 Progress & Feedback

- **Score** is always shown under the Check Answer button.
- The app tracks:
  - Total questions answered
  - Number of correct answers
  - Percentage score
- Exam mode shows a **final result report** with:
  - Overall percentage
  - Pass / Fail / Honours (80%+)
  - Per-category performance
  - Weak areas flagged if below 70%

---

## 🌐 Bilingual Interface (EN / FR)

From **Step 1**, the user can choose:

- 🇬🇧 **English**
- 🇫🇷 **Français**

The following elements switch language:

- All UI labels and instructions (steps, buttons, messages)
- Category names and report headings
- Pass/Fail labels and qualification text
- About / Support card content
- License notice & footer text

You can switch language **at any time**; the app updates instantly.

---

## 📱 Mobile-Friendly & PWA-Ready

- Single-page HTML app (no backend required)
- Responsive layout with a **mobile-optimized mode**
- Works well inside a browser or as a **Progressive Web App (PWA)** once hosted via GitHub Pages or similar
- Designed to be usable on phones, tablets, and desktops

---

## 🧭 Basic Usage (Steps Overview)

1. **Choose language (EN/FR).**  
2. **Load a question bank:**
   - Official Basic / Advanced from GitHub, or
   - Local TXT / CSV via “Choose a file”.
3. **Select a question mode:**
   - Random / No-repeat / Exam / Category Training.
4. **Click “Next Question”** to start, then “Check Answer” to see correctness (and explanations if using CSV).

You can use the **Reset** button (next to “Next Question”) to fully reset the app state and return to Step 1.

---

## 💬 About & Support

This free bilingual HAM Exam Trainer was created to help students prepare using real-style questions, official exam structures, and category statistics. It is licensed under **CC BY-NC-SA 4.0** (non-commercial, attribution, share-alike). You may use and share it for personal or educational purposes, but **not** resell it or include it in paid products or services.

If this app helps you and you’d like to support future improvements:

- ☕ Buy Me a Coffee: https://buymeacoffee.com/fabiolus  
- 💻 GitHub: https://github.com/Fabiolus2020/HamExamTrainer2025

---

## 📜 License (Summary)

This project is licensed under:

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**

You are free to:

- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

Under the following terms:

- **Attribution** — You must give appropriate credit to **Fabien Clermont**, provide a link to the license, and indicate if changes were made.
- **NonCommercial** — You may **not** use the material for commercial purposes.
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the **same license**.

Full legal text: https://creativecommons.org/licenses/by-nc-sa/4.0/

