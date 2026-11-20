# 🎓 ENT 301: Essentials of Entrepreneurship Study Portal

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)

A lightweight, interactive e-learning web application designed to help university students ma3ster the "Essentials of Entrepreneurship" (ENT 301) course. 

## 🚀 Live Demo
**Access the live study portal here:** [https://futafreshersguide.github.io/ENT301/](https://futaent301.netlify.app/)
or
**Access the live study portal here:** [https://futafreshersguide.github.io/ENT301/](https://futafreshersguide.github.io/ENT301/)

## 💡 The Motivation
The required textbook for this course is a massive 322 pages. For engineering students used to calculations, reading and cramming hundreds of pages of text is overwhelming. Furthermore, the exams include strict fill-in-the-gap questions requiring exact terminology. 

I built this portal to solve that problem. It replaces the need to blindly read the textbook by providing distilled chapter summaries, custom exam mnemonics, and a highly dynamic, JavaScript-powered Computer-Based Test (CBT) practice engine for immediate active recall. It was heavily used by my set during our 300 level and is scalable to other institutions offering similar entrepreneurship courses.

## 🌟 Features
*   **Distilled Chapter Summaries:** Condensed, easy-to-read notes highlighting the core concepts from Chapters 1 through 16.
*   **Mnemonics & Exam Hints:** Custom memory aids and crucial bullet points designed specifically for exam retention.
*   **Smart CBT Engine (Vanilla JS):** 
    *   Holds a massive question bank of **up to 200 questions per chapter** (thousands of questions in total).
    *   Dynamically shuffles and serves a random set of 60 questions per practice session using the Fisher-Yates algorithm.
    *   Supports Multiple Choice, True/False, and Fill-in-the-gap question formats.
*   **Instant Grading & Visual Feedback:** Automatically calculates scores, highlights correct/incorrect choices, and reveals answers for missed questions. Fill-in-the-gap inputs feature auto-capitalization and string validation.
*   **Integrated Materials:** Direct links to the original full-text course PDFs hosted on Google Drive.
*   **Direct Support:** Integrated floating WhatsApp button for students to ask questions directly.

## 🛠️ Tech Stack
*   **HTML5:** Semantic structure for accessible reading and form handling.
*   **CSS3:** Custom styling featuring a clean, responsive, distraction-free UI with CSS Grid/Flexbox and interactive hover states.
*   **Vanilla JavaScript (ES6+):** 
    *   Client-side array manipulation for randomizing the massive question banks.
    *   Dynamic DOM manipulation to render questions on the fly without page reloads.
    *   Form validation and string manipulation for accurate grading.

## 📂 Project Structure
*   `index.html`: The landing page featuring the course overview and a responsive chapter selection grid.
*   `chapter[X].html`: Individual chapter files (e.g., `chapter1.html` to `chapter15-16.html`). Each contains the specific chapter's summary and its unique 200-question JavaScript array bank.

## ⚙️ How the CBT Engine Works
The quiz engine is completely serverless and runs entirely client-side:
1. The `shuffleArray()` function randomizes the master `questionBank`.
2. The `.slice(0, 60)` method selects a random subset of 60 questions.
3. The `renderQuiz()` function dynamically generates the HTML for the questions based on their `type` (`mcq`, `tf`, or `fill`) and injects them into the DOM.
4. When `submitQuiz()` is fired, the script loops through the active questions, compares user inputs against the stored answers, applies CSS styling for visual feedback (green/red borders and text), and calculates the final percentage.

## 👨🏾‍💻 Author
Designed and Built by **Abideen Yakub Opeyemi (Ó'YẸMÍ)**  
*Federal University of Technology, Akure (FUTA)*
