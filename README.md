# 🎮 GameVault

A clean, beginner-friendly web portal designed to showcase and organize a personal collection of favorite video games. This project was developed as a hands-on practical assignment demonstrating end-to-end **Git & GitHub Version Control Workflows** and **Software Test Case Design**.

---

## 📌 Project Overview

**GameVault** serves as a lightweight, static web application containing:
- A **Home Page (`index.html`)** featuring introductory content and a curated list of popular games.
- An **About Page (`about.html`)** detailing the purpose of the platform along with contact information.
- A fully documented and version-controlled repository showcasing best practices in Git branching, merging, ignore rules, and commit history management.

---

## ✨ Features

- **Responsive Landing Page:** Clear introductory message and navigation.
- **Featured Games Catalog:** Displays a categorized list of titles (Minecraft, Valorant, GTA V).
- **Dedicated About & Contact Section:** Provides platform context and contact details (`contact@gamevault.com`).
- **Complete Git Version Control History:**
  - Standardized commit messages across all milestones.
  - Feature branching (`feature`) and clean integration into `main`.
  - Automatic exclusion of build/debug artifacts using `.gitignore`.
  - Clean history recovery demonstrated via `git revert`.
- **Software Quality Assurance:** An 8-point test case suite covering user authentication scenarios.

---

## 🛠️ Technologies Used

- **HTML5:** Semantic markup for structured page layout and navigation.
- **Git:** Distributed version control system used for local branching, commits, and history tracking.
- **GitHub:** Remote repository hosting and collaboration platform.
- **PowerShell:** Command-line shell utilized for environment setup and Git execution on Windows.

---

## 📁 Project Structure

```text
GameVault/
├── .git/                                         # Hidden Git repository metadata
├── .gitignore                                    # Ignores *.log files and temp/ directory
├── index.html                                    # Home page with Featured Games
├── about.html                                    # About page with Contact section
├── git_commands.txt                              # Reference list of all Git commands used
├── README.md                                     # Project overview and documentation
└── GameVault_Assignment_Report_VarunSandesh23.pdf # Final college submission report (Emerald theme)
```

> **Note on Ignored Files:**
> Files matching `*.log` (e.g., `debug.log`) and directories matching `temp/` are ignored by Git and excluded from remote synchronization.

---

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/VarunSandesh23/GameVault.git
   ```

2. **Navigate into the project directory:**
   ```bash
   cd GameVault
   ```

3. **Verify the Git status:**
   ```bash
   git status
   ```

---

## 🖥️ How to Run the Application

Because GameVault is built with pure static HTML, no complex server installation or build steps are required:

- **Option 1 (Direct in Browser):**
  Double-click `index.html` in your file explorer to open it in Google Chrome, Microsoft Edge, or any modern web browser.

- **Option 2 (Via PowerShell):**
  ```powershell
  Start-Process index.html
  ```

- **Option 3 (Live Server in VS Code):**
  Right-click `index.html` in Visual Studio Code and select **Open with Live Server**.

---

## 🔄 Git & GitHub Workflow Followed

The repository follows standard Git branching and version control practices:

1. **Repository Initialization:**
   ```powershell
   git init
   git branch -M main
   ```
2. **Initial Commit:** Staged and committed base `index.html` and `about.html`.
3. **Content Iteration:** Updated `index.html` with a featured games list.
4. **Feature Branch Isolation:**
   ```powershell
   git checkout -b feature
   # Added contact section to about.html
   git add about.html
   git commit -m "Add contact section to about.html"
   ```
5. **Merging into Main:**
   ```powershell
   git checkout main
   git merge feature
   ```
6. **Configuring Ignore Rules:** Added `.gitignore` to prevent tracking `*.log` files and the `temp/` folder.
7. **Safely Reverting Commits:** Added `temporary.txt`, committed it, and cleanly reverted it via:
   ```powershell
   git revert HEAD --no-edit
   ```
8. **Command Documentation:** Created and committed `git_commands.txt`.
9. **Remote Synchronization:** Linked local repository to GitHub and pushed both branches:
   ```powershell
   git remote add origin https://github.com/VarunSandesh23/GameVault.git
   git push -u origin main
   git push origin feature
   ```

---

## 🧪 Testing Details (Assignment Question 2)

As part of the assignment requirements, a comprehensive 8-scenario test suite was designed for a user login and authentication module:

| Test Case ID | Test Scenario | Input Data | Expected Result | Type | Status |
|---|---|---|---|---|:---:|
| **TC_LOG_01** | Valid credentials login | Valid username & password | Successfully authenticated; redirected to dashboard | Positive | **PASS** |
| **TC_LOG_02** | Invalid username & valid password | Unregistered username & valid password | Access denied; error: *"Invalid username or password"* | Negative | **PASS** |
| **TC_LOG_03** | Valid username & wrong password | Valid username & incorrect password | Access denied; error: *"Invalid username or password"* | Negative | **PASS** |
| **TC_LOG_04** | Blank username submission | Empty username & valid password | Form blocked; validation: *"Username cannot be empty"* | Boundary | **PASS** |
| **TC_LOG_05** | Blank password submission | Valid username & empty password | Form blocked; validation: *"Password cannot be empty"* | Boundary | **PASS** |
| **TC_LOG_06** | Both fields blank submission | Empty username & empty password | Form blocked; validation: *"Please fill in all required fields"* | Boundary | **PASS** |
| **TC_LOG_07** | Password masking & visibility toggle | Password text + toggle action | Masked with dots by default; toggles to clear text on click | UI / UX | **PASS** |
| **TC_LOG_08** | Account lockout protection | 5 consecutive wrong password attempts | Account locked for 15 minutes; alert notification shown | Security | **PASS** |

---

## 👤 Author Details

- **Name:** Varun Sandesh
- **GitHub:** [@VarunSandesh23](https://github.com/VarunSandesh23)
- **Repository:** [https://github.com/VarunSandesh23/GameVault](https://github.com/VarunSandesh23/GameVault)
