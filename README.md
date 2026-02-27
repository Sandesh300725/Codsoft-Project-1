# 🤖 Simple Python Chatbot

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![No Libraries](https://img.shields.io/badge/Libraries-None-brightgreen?style=for-the-badge)
![Terminal](https://img.shields.io/badge/Interface-Terminal-black?style=for-the-badge&logo=windows-terminal)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)
![Beginner Friendly](https://img.shields.io/badge/Level-Beginner%20Friendly-orange?style=for-the-badge)

<br/>

> **A simple rule-based terminal chatbot built with pure Python — no libraries, no API keys, just Python and your keyboard.**

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [How It Works](#-how-it-works)
- [Installation](#️-installation)
- [Usage](#-usage)
- [Sample Conversation](#-sample-conversation)
- [Supported Commands](#-supported-commands)
- [Project Structure](#-project-structure)
- [Customization](#-customization)
- [Roadmap](#️-roadmap)
- [License](#-license)

---

## 🧠 Overview

This is a beginner-friendly **rule-based chatbot** written in Python. It runs entirely in the terminal and responds to common conversational inputs using simple keyword matching — no machine learning, no internet connection, no external libraries required.

It's a great starting project to understand how chatbots work at a fundamental level before diving into NLP or AI-powered bots.

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 **Conversational Replies** | Responds to greetings, questions, and small talk |
| 😂 **Tells Jokes** | Includes a built-in joke response |
| 🕐 **Time Aware** | Can respond to time-related queries |
| 🔄 **Continuous Loop** | Keeps chatting until you say "bye" |
| ⚡ **Zero Dependencies** | Uses only Python's built-in `time` module |
| 🟢 **Beginner Friendly** | Clean, readable code — perfect for learning |

---

## ⚙️ How It Works

```
User types a message
        │
        ▼
Input is converted to lowercase
        │
        ▼
chatbot() checks for keywords using if/elif conditions
  ├── "hi" / "hello"         → Greeting response
  ├── "what is your name"    → Name response
  ├── "how are you"          → Wellbeing response
  ├── "hobbies" / "interests"→ Hobby response
  ├── "eat" / "food"         → Food response
  ├── "favorite color"       → Color response
  ├── "music"                → Music response
  ├── "joke"                 → Tells a joke
  ├── "weather"              → Weather disclaimer
  ├── "news"                 → News disclaimer
  ├── "translate"            → Translation disclaimer
  ├── "time"                 → Returns current time
  ├── "bye"                  → Exits the chat loop
  └── (anything else)        → Fallback message
        │
        ▼
Response is printed to the terminal
```

---

## 🛠️ Installation

No installation required! Just make sure you have Python installed.

### Step 1 — Check Python Version
```bash
python --version
# Should show Python 3.x
```

### Step 2 — Clone or Download the Project
```bash
git clone https://github.com/YOUR_USERNAME/simple-python-chatbot.git
cd simple-python-chatbot
```

### Step 3 — Run the Chatbot
```bash
python chatbot.py
```

That's it! No `pip install` needed. 🎉

---

## 🚀 Usage

Run the script in your terminal:

```bash
python chatbot.py
```

You'll see:
```
Chatbot: Hi! I'm a simple chatbot, I'm here to assist you!
Me: 
```

Type your message and press **Enter**. Type `bye` to exit.

---

## 💬 Sample Conversation

```
Chatbot: Hi! I'm a simple chatbot, I'm here to assist you!

Me: hello
Chatbot: Hi there! I'm a chatbot here to assist you.

Me: what is your name
Chatbot: I'm just a chatbot, so I don't have a name, but you can call me anything.

Me: tell me a joke
Chatbot: Why did the scarecrow win an award? Because he was outstanding in his field!

Me: what is the time now
Chatbot: It's 5:00 PM

Me: what is the weather in Mumbai
Chatbot: I'm sorry, I don't have real-time weather data.

Me: bye
Chatbot: Goodbye! Have a great day!
```

---

## 📋 Supported Commands

| What You Type | What Friday Replies |
|---|---|
| `hi` / `hello` | Greeting message |
| `what is your name` | Chatbot introduces itself |
| `how are you` | Wellbeing reply |
| `do you have any hobbies` / `interests` | Hobby reply |
| `what did you eat today` / `what do you like to eat` | Food reply |
| `favorite color` | Color preference reply |
| `do you enjoy listening to music` | Music reply |
| `tell me a joke` / `another joke` | Tells a joke 😄 |
| `tell me an interesting fact` | Fact reply |
| `weather in [city]` | Weather disclaimer |
| `latest news` | News disclaimer |
| `translate` | Translation disclaimer |
| `what is the time now` | Returns the time |
| `bye` | Ends the conversation |
| *(anything else)* | Fallback / didn't understand |

---

## 🗂️ Project Structure

```
simple-python-chatbot/
│
├── chatbot.py       # Main chatbot script
└── README.md        # Project documentation
```

---

## 🎨 Customization

### Add a New Response
Open `chatbot.py` and add a new `elif` block inside the `chatbot()` function:

```python
elif "your keyword" in user_input:
    return "Your custom reply here!"
```

**Example — Add a motivational quote:**
```python
elif "motivate me" in user_input or "quote" in user_input:
    return "Believe you can and you're halfway there. — Theodore Roosevelt 💪"
```

### Fix the Time Response
Currently the time is hardcoded. Replace it with a live time using the `time` module:

```python
elif "what is the time now" in user_input:
    return f"The current time is {time.strftime('%I:%M %p')}"
```

### Make It Case-Sensitive Friendly
The bot already converts input to lowercase with `user_input.lower()`, so users can type in any case and it will still work.

---

## 🛣️ Roadmap

- [x] Basic keyword matching responses
- [x] Continuous chat loop with exit command
- [x] Lowercase input normalization
- [ ] Fix live time using `time.strftime()`
- [ ] Add more jokes and facts
- [ ] Connect to OpenWeatherMap API for real weather
- [ ] Connect to NewsAPI for real news headlines
- [ ] Add Wikipedia search integration
- [ ] Build a GUI version using Tkinter
- [ ] Upgrade to NLP-based responses using NLTK or spaCy
- [ ] Connect to OpenAI API for GPT-powered replies

---

## 📄 License

This project is licensed under the **MIT License** — free to use, modify, and share.

---

<div align="center">

⭐ **If this helped you learn Python, give it a star!** ⭐

*Built with ❤️ and Python*

</div>
