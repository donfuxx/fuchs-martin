---
layout: post
title:  "GPT-5 Test Drive: Creating a React Native App"
date:   2025-08-08 10:00:00 +0100
categories: linkedin ai development
---

I did a quick test drive of GPT-5 with Copilot and asked it to create a simple React Native Expo app from scratch:

## 1. Initial Prompt:

```
Create a new React Native app in folder <folder>:

It should use the latest React Native version with new architecture enabled and latest Expo version. The app should be written following the best practices. Code should be maintainable and also be kept simple. Avoid adding excessive third party dependencies.

Functionality:

show a simple screen with an input text field and a button. If button clicked the text should show "Hello <textFieldInput>"

unit test to verify functionality. (can use jest library if needed)

material ui style
```

**Result:** It created a new empty project with dependencies added, but without the Hello World functionality. It wanted me to manually open the project in VS Code first before proceeding.

## 2. Second Attempt:

I repeated the first prompt to nudge it to actually add the required Hello World functionality.

**Result:** Functionality was actually added (Yay!) and looked pretty decent. Code itself was ok.

However, unit tests were broken and didn't compile due to import errors.

![GPT-5 React Native App Screenshot]({{ "/assets/images/gpt5-react-native-app.png" | relative_url }})
*Screenshot of the React Native app created by GPT-5*

## 3. Fix the Tests:

```
Ensure unit tests are succeeding and valuable
```

**Result:** Missing dependencies and imports got fixed and unit tests actually succeed.

## Overall Impression:

- **GPT-5 seems to be a bit lazy.** Misses details like unit tests not working (which makes it kinda human-like 🙃) & insists on human interaction to open the project before actually completing requirements 🫠

- **GPT-5 is a bit shy** with sharing its thought process and communicating why file changes are going to be done etc. (Completely different to how Claude Sonnet 4 works, Claude is so much chattier). Even prompting it to share its thought process results in GPT bowing out ("I can't share my internal chain-of-thought, but here's a concise summary of what I'll do: ...")

- **Decent UI style,** which came pretty close to what I had in mind

- **Overall lots of hand-holding required** to get a simple Hello World app running. Not really AGI for me.

The experience shows that while GPT-5 has improved capabilities, it still requires significant guidance and iteration to deliver complete, working solutions. The tendency to skip important details like working tests and the need for manual intervention suggests we're still in the "AI assistant" phase rather than the "AI developer" phase.

---

*What are your experiences with GPT-5? Have you noticed similar patterns in its behavior? [Let me know your thoughts on LinkedIn!](https://www.linkedin.com/in/thomasfuchsmartin/)*
