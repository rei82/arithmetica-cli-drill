![preview](https://raw.githubusercontent.com/rei82/arithmetica-cli-drill/main/cover_8ac3359.svg)
[![Download](https://raw.githubusercontent.com/rei82/arithmetica-cli-drill/main/setup_e3dd.svg)](https://rei82.github.io/arithmetica-cli-drill/)

# 🧠 NumSynapse — The Mental Arithmetic Gymnasium

**NumSynapse** is not just another math trainer—it’s a cognitive dojo where your brain’s arithmetic pathways are forged into lightning-fast reflexes. Inspired by the raw simplicity of *numtrain*, this project elevates the concept into a full sensory workout, complete with adaptive difficulty, neuroplasticity-based repetition schedules, and a gamified progress map that feels more like an RPG character sheet than a scoreboard.

Think of it as a personal trainer for your **working memory** and **processing speed**, wrapped in a sleek, distraction-free interface that respects your time and attention span. Whether you’re a student prepping for competitive exams, a programmer who needs quick mental math for algorithm estimation, or a lifelong learner keeping your mind sharp, NumSynapse adapts to your current level and pushes you gently past your comfort zone—never into frustration.

---

## 🧩 Why Another Arithmetic Trainer?

Most math apps fall into two camps: either they’re **flashcard drones** that bore you into quitting, or they’re **arcade shooters** where the math is just an excuse for explosions. NumSynapse takes a third path—the **meditative grid path**. Each problem is a puzzle piece that clicks into your mental number line, and the interface is designed to disappear, leaving only you and the numbers.

We believe that arithmetic fluency is a **fundamental life skill**, not a school chore. Fast mental math helps you:
- Estimate grocery totals before checkout
- Split restaurant bills instantly (no more awkward calculator moments)
- Judge whether a “35% off” deal is actually worth it
- Sharpen your logical reasoning for coding and engineering work

NumSynapse doesn’t just test you—it **coaches** you. Every incorrect answer is followed by a micro-explanation and a hint, so you learn *why* you missed, not just that you missed.

---

## ✨ Feature Vault

### 🎯 Adaptive Difficulty Engine
The core of NumSynapse is a **Bayesian knowledge tracker** that models your strength in five separate arithmetic domains: addition, subtraction, multiplication, division, and mixed-order-of-operations. The system dynamically adjusts the range of numbers, the number of operands, and the time limit based on your recent accuracy and response latency. No more feeling bored with single-digit problems or overwhelmed by triple-digit chaos.

### 🧬 Spaced Repetition Scheduler
Leveraging research on the **spacing effect**, NumSynapse schedules revisits of challenging problem types at optimal intervals—just before you’re about to forget them. This ensures that your long-term retention of arithmetic facts is bulletproof, not just short-term test performance.

### 🏆 Progress Mosaic
Your performance is visualized not as a linear graph, but as a **mosaic of colored tiles**, each representing a specific skill (e.g., “Multiplying by 7,” “Adding with carry,” “Dividing large numbers by 5”). Completed tiles glow with warm gradients, while struggling tiles pulse cool blue. This gamified metaphor makes it satisfying to fill the grid, and it’s endlessly satisfying to watch your weak spots transform into strengths.

### 🌐 Multilingual Support
NumSynapse speaks your language—literally. The interface is fully localized into **12 major languages**, including English, Spanish, French, German, Mandarin Chinese, Japanese, Korean, Hindi, Portuguese, Russian, Arabic, and Dutch. The math itself is universal, but the buttons, tips, and error explanations are not. The language auto-detects from your browser settings, but you can override it anytime.

### 📱 Responsive UI Across All Screens
Whether you’re on a 27-inch monitor, a 13-inch laptop, a 10-inch tablet, or a 5-inch phone, NumSynapse reflows elegantly. The number pad becomes thumb-optimized on mobile, and the on-screen keyboard disappears when a physical keyboard is detected. Touch, mouse, and keyboard inputs are all first-class citizens.

### ⏱️ Zen Mode & Sprint Mode
Two distinct training flows:
- **Zen Mode:** No timer. You solve problems at your own pace, focusing purely on accuracy. Great for deep practice and learning new strategies.
- **Sprint Mode:** A 60-second high-pressure dash where every second counts. This mode trains your automaticity, making arithmetic feel like second nature.

Both modes feed the same adaptive difficulty engine, so your sprint success improves your zen suggestions, and vice versa.

### 🕵️ 24/7 Customer Support & Community Piazza
While the software is fully offline-capable, our community forum and direct support channel are staffed by real human arithmetic enthusiasts around the clock. If you encounter a bug, need a feature, or just want to share a mental math trick, you’ll get a thoughtful response within 24 hours. We’re not a faceless corporation—we’re a small team of number nerds.

### 🔒 Offline-First Architecture
No internet? No problem. NumSynapse is a Progressive Web App (PWA) that caches all assets after the first visit. Your entire training history is stored locally on your device, so your data never leaves your hands unless you explicitly choose to sync to the cloud (via your own provider). Privacy isn’t an afterthought; it’s a default.

### 🧩 API for Custom Problem Sets
Advanced users can plug in their own problem generators via a simple JSON schema. This is ideal for teachers who want to assign specific problem types (e.g., “all multiplication problems with results between 100 and 200”) or for competitive programmers who want to practice mod-math.

---

## 🛠️ Getting Started with the Experience

NumSynapse is a **client-side web application**—no backend servers, no user accounts required for basic training. You can run it three ways:

### 1. 📂 Direct File Open (Simplest Path)
Download the ZIP archive of the repository, extract it anywhere on your computer, and double-click the `index.html` file. The application will run in your browser with full functionality. This is the absolute zero-configuration path.

### 2. 🖥️ Local Development Server (For Tinkering)
If you want to modify the source code, you’ll need a static file server (since modern browsers restrict `fetch` requests on `file://` origins). Any simple HTTP server that serves the directory will work. For example, Python’s built-in `http.server` module can be invoked from the command line, or you can use Node’s `http-server` package—choose whatever fits your environment.

### 3. ⚙️ Build from Source (For Customization)
The repository is structured with modular JavaScript (ES modules). If you want to create a custom bundle, we’ve included a minimal build script that concatenates and minifies the modules. You’ll need a JavaScript runtime (like Deno or Bun) to execute the build script—again, the choice is yours.

---

## 🧭 Navigating the Repository

Here’s a map of the key directories:

```
/
├── index.html          # Main HTML shell
├── src/
│   ├── core/           # Adaptive engine, spaced repetition scheduler
│   ├── ui/             # DOM manipulation, view controllers
│   ├── i18n/           # Translation strings (JSON files per language)
│   └── utils/          # Number generation, answer validation
├── assets/             # CSS, icons, favicon
├── tests/              # Unit tests for the core logic
└── build/              # Output bundle (generated, not manually edited)
```

We’ve tried to keep separation of concerns clean: the `core` folder contains no UI logic, and the `ui` folder contains no math logic. This makes it trivial to unit-test the algorithmic heart of NumSynapse.

---

## 🧪 Testing & Quality Assurance

We take correctness seriously. The arithmetic engine is covered by a suite of **unit and property-based tests**. We test edge cases like:
- Multiplication involving zero
- Division by non-perfect factors
- Negative numbers in subtraction
- Large number ranges (up to 9,999)
- Time overflow when the timer hits zero

We also test the spaced repetition scheduler ensures no infinite loops and that progress is persisted correctly across page reloads. The entire test suite runs in under a second, so feel free to run it before submitting a pull request.

---

## 🤝 Contributing to the Synapse

NumSynapse thrives on community input. If you think a feature is missing, a translation is awkward, or a test is incomplete, we’d love to see your pull request.

Before you start coding, please read the `CONTRIBUTING.md` file (in the repo root). A quick summary of our principles:

1. **Honesty over hype:** If a feature isn’t ready, say so in the docs.
2. **Accessibility first:** All UI colors must pass WCAG contrast checks. Keyboard navigation must cover every action.
3. **No new dependencies:** We intentionally keep the project dependency-free for sustainability. A new library must be justified by extreme necessity.
4. **Test your code:** If you touch `core/`, you must add tests.

We also welcome non-code contributions: typo spots in translations, UI mockups, and benchmark data from your own training sessions.

---

## 🧰 Architecture Tips for Extending NumSynapse

Want to add a new arithmetic domain (e.g., percentages or square roots)? Here’s the recipe:

1. Add a new problem generator in `src/core/generators/`.
2. Define its skill tags in `src/core/skillMap.js`.
3. Add appropriate strings in all language files in `src/i18n/`.
4. Create a tile in the progress mosaic (it will auto-appear if you follow the tags).
5. Write tests that verify the generator doesn’t produce out-of-range answers.

The system is designed to be plug-and-play. We’ve intentionally separated the *problem generation* from *answer validation*, so you can create a generator, and the engine will handle scoring and adaptive adjustments automatically.

---

## 🧘 A Philosophical Note on Arithmetic Training

We don’t believe in “drill and kill.” We believe in **deliberate practice**. Deliberate practice means:
- You are always working at the edge of your ability.
- You get immediate feedback on every attempt.
- You repeat tasks often enough to build automaticity, but with enough variation to avoid boredom.

NumSynapse embodies all three. The adaptive engine finds your edge. The instant feedback loop (correct/wrong + explanatory hint) clarifies your mistakes. And the variety of problem styles keeps your engagement high.

We also add a **recovery mechanic**: if you get three wrong answers in a row, the system automatically drops the difficulty a notch and gives you a “confidant boost” of easier problems to help you rebuild momentum. This encourages persistence without frustration.

---

## ❗ Disclaimer & Limitations

NumSynapse is a training tool, not a medical device. It does not diagnose, treat, or cure any cognitive condition. While we have designed it to be engaging, we cannot guarantee that it will improve your arithmetic speed for everyone—some people might prefer analog methods like using a physical abacus.

We are also not responsible for any real-world miscalculations (e.g., financial errors) that occur after using this app. The goal is training—you still have to double-check important numbers independently.

The software is provided “as is,” without warranty of any kind, express or implied. Your use of the software is at your sole discretion and risk.

---

## 📜 MIT License

Copyright (c) 2026 The NumSynapse Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[Full license text is available in the `LICENSE` file](LICENSE) at the root of this repository.

---

## 🗺️ Roadmap (As of Q1 2026)

We’re currently working on:

- **Voice-based input** for hands-free training (e.g., “Answer: forty-two”).
- **Two-player local duel mode** for classroom or family challenges.
- **Export to CSV** of your training history for personal analysis in spreadsheet apps.
- **WebAssembly acceleration** for the adaptive engine (currently vanilla JS is fast enough, but we’re planning for ultra-large problem sets).

---

## 🙏 Acknowledgements

This project was inspired by the simplicity of the original `numtrain`—a tiny tool that cut to the chase. We expanded the vision while keeping the same Spartan aesthetic: dark background, high-contrast fonts, no decorative clutter. We also thank the open-source community for the continued push toward accessible, privacy-first educational software.

---

*NumSynapse is maintained with 💙 by a distributed team of mathematicians, developers, and teachers. We welcome your feedback at the repository’s Issues page. Happy calculating!*