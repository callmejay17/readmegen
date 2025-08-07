# 📝 ReadMeGen

**ReadMeGen** is a fast and minimal CLI tool that lets you instantly generate beautiful `README.md` files for your projects — right from the terminal.

Whether you're a developer, hacker, student, or indie maker, ReadMeGen makes it easy to kickstart any project with a clean and consistent README.

---

## 🚀 Features

- 📄 Auto-generate `README.md` with project details
- 🎯 Includes badges (language, license)
- 🧠 Supports multiple languages (Python, Node.js, Rust — more coming)
- 📦 Outputs directly to a ready-to-push file

---

## 📦 Installation

```bash
# Clone the repo
$ git clone https://github.com/callmejay17/readmegen.git
$ cd readmegen

# Install locally
$ pip install .
```

---

## ⚙️ Usage

```bash
readmegen create --project "my-awesome-tool" --lang python --license MIT --description "A cool CLI tool." --badges
```

This will create a `README.md` like:

```markdown
# my-awesome-tool

![License](https://img.shields.io/badge/license-MIT-blue)
![Language](https://img.shields.io/badge/language-python-yellow)

## 📝 Description
A cool CLI tool.

## 🚀 Installation
```bash
$ git clone https://github.com/callmejay17/my-awesome-tool.git
$ cd my-awesome-tool
```

## 📦 Usage
```bash
$ python main.py
```

## 📄 License
This project is licensed under the MIT license.
```

---

## 🛠 Roadmap
- [ ] Add support for project-specific sections
- [ ] Export as PDF or DOCX
- [ ] GUI version (TUI)
- [ ] AI-generated README templates

---

## 🧠 Author
**** — [@jay](https://github.com/callmejay17)

---

## 📄 License
MIT
