# SessionSwitch-Multi-Account-Browser-Extension

A full-stack browser extension & backend for seamless multi-account management. Save, restore, and synchronize complete web sessions (cookies, localStorage, sessionStorage) across devices, enabling quick switching between user profiles with secure authentication.

[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/SessionSwitch-Multi-Account-Browser-Extension/ci.yml?style=flat-square&logo=githubactions)](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/SessionSwitch-Multi-Account-Browser-Extension?style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/SessionSwitch-Multi-Account-Browser-Extension)
[![Tech Stack](https://img.shields.io/badge/tech-stack-Node.js%2C%20JavaScript%2C%20MongoDB-blue?style=flat-square&logo=javascript)](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension)
[![Lint/Format](https://img.shields.io/badge/lint--format-ESLint%2CBelInternal-orange?style=flat-square&logo=eslint)](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension)
[![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-red?style=flat-square&logo=creativecommons)](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension/blob/main/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/SessionSwitch-Multi-Account-Browser-Extension?style=flat-square&logo=github)](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension)

---

**This project provides a robust solution for managing multiple browser accounts and sessions, enhancing productivity and simplifying workflows for users who frequently switch between different profiles or contexts.**

## Architecture

mermaid
graph TD
    A[Browser Extension] -- API Calls --> B(Backend API)
    B -- CRUD Operations --> C(MongoDB Database)
    A -- Session Data --> C
    D[Authentication Service] -- Verify/Manage --> B
    A -- Sync --> B


## Table of Contents

*   [Architecture](#architecture)
*   [Features](#features)
*   [Getting Started](#getting-started)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)
*   [Support](#support)
*   [🤖 AI Agent Directives](#ai-agent-directives)

---

## Features

*   **Session Saving:** Securely store active browser sessions, including cookies, `localStorage`, and `sessionStorage`.
*   **Session Restoration:** Quickly restore saved sessions to a clean browser profile.
*   **Cross-Device Synchronization:** Sync sessions across multiple devices via the backend.
*   **Multi-Account Management:** Seamlessly switch between different user accounts for various web services.
*   **Secure Authentication:** Robust authentication for backend access and session management.
*   **Productivity Boost:** Minimize context-switching overhead and time spent logging into multiple accounts.

---

## Getting Started

### Prerequisites

*   Node.js (v18+ recommended)
*   npm or yarn
*   MongoDB instance (local or cloud)

### Installation

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension.git
    cd SessionSwitch-Multi-Account-Browser-Extension
    

2.  **Backend Setup:**
    *   Navigate to the `backend` directory:
        bash
        cd backend
        
    *   Install dependencies:
        bash
        npm install
        
    *   Configure environment variables (e.g., `JWT_SECRET`, `MONGODB_URI`) in a `.env` file.
    *   Start the backend server:
        bash
        npm start
        

3.  **Extension Setup:**
    *   Navigate to the `extension` directory:
        bash
        cd ../extension
        
    *   Install dependencies:
        bash
        npm install
        
    *   Configure the extension to connect to your backend API (update `API_URL` in relevant config files).
    *   Load the extension in your browser (e.g., Chrome: `chrome://extensions/`, enable Developer Mode, click 'Load unpacked', select the `extension` directory).

---

## Development

### Scripts

| Script        | Description                                            |
|---------------|--------------------------------------------------------|
| `npm install` | Installs project dependencies.                         |
| `npm run dev` | Starts the development server for backend and extension. |
| `npm run build`| Builds production-ready artifacts.                     |
| `npm run test` | Runs unit and integration tests.                       |

### Principles

*   **SOLID:** Ensure code is maintainable and scalable.
*   **DRY:** Avoid code duplication.
*   **YAGNI:** Implement only necessary features.
*   **Security First:** Prioritize secure coding practices, especially with sensitive session data and authentication.

---

## Contributing

We welcome contributions! Please refer to the [CONTRIBUTING.md](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension/blob/main/.github/CONTRIBUTING.md) file for guidelines on how to submit pull requests and report issues.

---

## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0). See the [LICENSE](https://github.com/chirag127/SessionSwitch-Multi-Account-Browser-Extension/blob/main/LICENSE) file for more details.

---

## Support

For support, please open an issue on the GitHub repository.

---

## 🤖 AI Agent Directives

<details>
  <summary>View Agent Directives</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (JavaScript/TypeScript)**
    *   **Stack:** This project leverages **JavaScript (ES6+)** with **Node.js** for the backend and a browser extension environment. Key tools include **npm** (package management), **ESLint** (linting), and **Jest** (testing).
    *   **Architecture:** Employing a **Full-Stack** architecture. The browser extension handles UI and local storage, communicating with a **Node.js/Express.js backend** for API operations and data persistence. **MongoDB** serves as the primary database.
    *   **Security:** Emphasize secure authentication (e.g., JWT) and secure handling of sensitive browser session data (cookies, localStorage).
    *   **Browser Extension Framework:** Utilize standard browser extension APIs and potentially a framework like `WebExtension Toolkit (WXT)` for streamlined development if deemed necessary in late 2025 standards.

*   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go) - *Not applicable***

*   **TERTIARY SCENARIO C: DATA / AI / SCRIPTS (Python) - *Not applicable***

---

## 4. DEVELOPMENT STANDARDS & VERIFICATION
*   **Code Quality:** Adhere to **SOLID** principles for maintainable code. Ensure **DRY** (Don't Repeat Yourself) and **KISS** (Keep It Simple, Stupid) where appropriate.
*   **Testing Strategy:** Comprehensive unit tests using **Jest** for both backend and extension logic. Integration tests to verify backend API endpoints and database interactions. End-to-end tests for core user flows (saving, restoring, switching sessions).
*   **Linting & Formatting:** Enforce consistent code style using **ESLint** and **Prettier**. Auto-formatting should be applied via pre-commit hooks.
*   **Build Process:** Implement a robust build process using **npm scripts** for development, testing, and production builds. For the extension, ensure proper manifest file generation and bundling.
*   **Dependency Management:** Utilize **npm** for managing project dependencies. Regularly audit dependencies for security vulnerabilities.

---

## 5. VERIFICATION COMMANDS

*   **Backend Tests:**
    bash
    cd backend
    npm run test
    

*   **Extension Tests:**
    bash
    cd extension
    npm run test
    

*   **Linting (Backend):**
    bash
    cd backend
    npm run lint
    

*   **Linting (Extension):**
    bash
    cd extension
    npm run lint
    

*   **Formatting (Backend):**
    bash
    cd backend
    npm run format
    

*   **Formatting (Extension):**
    bash
    cd extension
    npm run format
    

</details>
