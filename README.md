# ⬡ Artifact Recall Management (ARM)

Consider the conceptual body; When someone helps you stand they join your feet, like a philosophers shoes made of truths. When they help you think they join your head like AI processing. When they help you do they join your ARMs. 
Have a habit of making chats with artifacts and forgetting to save them? then never able to remember where they went?
Have hundreds of chats that RAG cannot find?
So do I

ARM begun as a simple artifact sorting tool for Claude since its artifact list has no semblance of order, it turned into a project-artifact viewing system because keeping track of artifacts is impossible with memory loss issues.

This is an autonomous Chrome Extension for enhancing the **Claude.ai** and **Gemini** experience. This tool provides advanced artifact management, real-time sorting, and AI-powered summarization, all while preserving the integrity of your original chat flow.

This project exists because the native experience is fundamentally broken for power users. What started as a simple fix for a disorganized list has been built out into a comprehensive **Project-Artifact Viewing System**. This extension treats your artifacts as an indexed database rather than a pile of discarded drafts. It’s about taking control of the chaos and turning it into a searchable archive that actually remembers what you did—even when you (and AI) have reached the limits of your memory.

---

## 🚀 Installation Guide

### 1. Download the Extension
- Click the green **Code** button on GitHub and select **Download ZIP**.
- Extract the ZIP file to a folder on your computer (e.g., `Documents/artifact-recall-management`).

### 2. Open Extensions Page
In most Chromium-based browsers, typing `chrome://extensions` will automatically redirect you to the correct internal page.

**Compatible Browsers:**
- **Chrome**: `chrome://extensions`
- **Edge**: `edge://extensions`
- **Brave**: `brave://extensions`
- **Vivaldi / Opera / Sidekick / Arc / Orion**: (Any Chromium-based browser)

### 3. Enable Developer Mode
- In your browser's Extensions page, toggle the **Developer mode** switch (usually in the top-right or sidebar) to **ON**.

### 4. Load the Extension
- Click the **Load unpacked** button.
- In the file picker, select the folder containing `manifest.json`.
- **Artifact Recall Management** should now appear in your list of extensions.

---

## 📖 How to Use

### 1. Indexing Your Chats
To "document" a chat and its artifacts into the **Project Review** system, simply navigate to that chat. ARM will automatically scan the messages and sidebars to build its local database for that specific conversation.

### 2. Live Artifact Generation
Once you are inside a chat, ARM remains active. Any new artifacts the model generates will be automatically detected, indexed, and added to the Sorter Panel and Sidebar in real-time.

### 3. Troubleshooting & Refreshing
If the UI becomes "stuck" or you don't see a newly generated file immediately, simply click the **↺ (Rescan)** button in the floating panel. This forcibly re-synchronizes the extension with the page's current DOM.

---

## ✨ Features

### 🖱️ Advanced Sorter Panel
- **Tabbed Interface**: Switch between **This Chat** (current context) and **Project Review** (your entire project history).
- **Hybrid Recognition**: Detects artifacts in real-time as they generate, whether the sidebar is open or closed.
- **Quick Interactions**: 
    - **Single-Click**: Jump to and highlight the artifact (Gold Pulse highlight in chat).
    - **Double-Click**: Open the artifact content directly in the main view.
- **Multidimensional Sorting**: Sort by Filename (A-Z/Z-A), File Size, File Type, or "First Seen" Timestamp.


### 📂 Project-Wide Browser
- **Persistent Index**: ARM archives every chat it scans within a project (via UUID extraction).
- **Archive Stats**: View artifact counts, last-seen timestamps, and chat names for everything you've worked on in one view.
- **Lazy-Rendered Previews**: Expand any past chat in the list to view its artifacts and AI summaries without leaving the current chat.
- **Deep Navigation**: ↗ icons allow for instant navigation to past chats in new tabs with a single middle-click.

### 🧠 Smart AI Summaries
- **Targeted Prompting**: ARM intelligently ignores already-summarised files, generating prompts **only for new/unsummarised artifacts**, saving context and tokens.
- **Inline Sidebar Injection**: Inject summaries directly into the Sidebar metadata area for a frictionless overview of your file history.
- **Summarise Badge**: A smart badge (`N new — summarise?`) pulses gold when new files need attention.

### 🛡️ Chat Space Protection
- **Immutable Chat Flow**: ARM is strictly non-intrusive. It **never** injects structural DOM elements into the main chat flow, protecting your exports and screenshots from clutter.
- **Sidebar Scoping**: Sorting controls and summary badges are strictly scoped to the Artifacts Sidebar.

## Change.log
- **Artifact Chat Summary Search**: Search your artifact list and summaries for hits
- **Non-project sort support**: Added non-project support, whoops
- **Chat-Summaries**: Summarise your chats and inject them into the sort panel
- *Something else I probably forgot: I'm sure there was something else and there usually is*

# I Should Probably;
- Add the timestamps into the sidebar
---

## 🛠️ Usage Tips
- **The Gold Pulse**: The `⬡` toggle button in the header will pulse gold when a new artifact is caught by the background scanner.
- **JSON Formatting**: When summarising, the model provides a JSON object which ARM automatically parses and maps back to your files.
- **Manual Scan**: Click **↺** in the Sorter Panel or Sidebar to force a full re-index of the current view.
<img width="1131" height="856" alt="Screenshot 2026-04-10 042853" src="https://github.com/user-attachments/assets/e9045b24-c03b-4c65-b997-bb51328da9f4" />

---

*Note: This extension is designed for personal use and is not affiliated with Anthropic or Google.*
