# Outfit Buddy – The AI-Powered Sustainable Stylist 👔👗

**Outfit Buddy** is a context-aware web application that functions as your personal AI stylist. It solves decision fatigue by proactively suggesting optimal outfits based on your **Outlook Calendar** schedule and **Local Weather** conditions, while promoting sustainable fashion habits.

---

## 📖 Table of Contents
- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Key Features](#-key-features)
- [Tech Stack & Architecture](#-tech-stack--architecture)
- [Getting Started](#-getting-started)
- [Team](#-team)

---

## 🧩 The Problem
**"I have nothing to wear."**
Even with a full closet, many people suffer from:
*   **Decision Fatigue:** Wasting time in the morning trying to choose an outfit.
*   **Context Disconnect:** Dressing incorrectly for the weather (e.g., canvas shoes in the rain) or occasion (casual wear to a client meeting).
*   **Asset Underutilization:** Using only ~20% of the wardrobe effectively.
*   **Sustainability Gap:** High-quality clothes sit unused instead of being donated.

## 💡 The Solution
**Outfit Buddy** utilizes an AI agent to aggregate your wardrobe inventory with external context. It filters out unsuitable items and ranks the rest based on formality and rotation frequency to suggest the perfect outfit.

> *"It’s rainy and you have a dinner date → Wear the leather loafers, not the canvas shoes."*

---

## ✨ Key Features

### 📅 Context Awareness
Syncs directly with **Outlook Calendar** and **Weather APIs**. The app knows if you have a "Weekly Standup" or a "Dinner Date" and checks the forecast (e.g., 13°C & Rainy) to ensure comfort and appropriateness.

### 🤖 AI Stylist & Recommendation Engine
*   **Smart Suggestions:** Applies custom filtering algorithms to exclude items unsuitable for the weather.
*   **Ranking System:** Prioritizes items based on formality (0-10 scale) and "Last Worn Date" to maximize wardrobe rotation.

### 🧥 Smart Wardrobe Management
*   **Scan with AI:** Easily add new items. The AI automatically tags attributes like Fabric, Pattern, Category, and rates them on Formal, Warmth, and Relaxed scales.
*   **Digitized Inventory:** View your Tops, Bottoms, Shoes, and Accessories in a clean dashboard.

### 🌍 Sustainability ("Your Impact")
Promotes circular fashion by tracking item utility. It highlights clothes you haven't worn in a while (e.g., *"Beige Trench Coat - Not worn recently"*) and provides a direct **"Find Donation Center"** button.

---

## 🛠 Tech Stack & Architecture

The solution is built on a robust **Hybrid Cloud Architecture**, leveraging Microsoft Azure and Google Firebase.

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | **Next.js** | React framework for a fast, server-side rendered (SSR) UI. |
| **Hosting** | **Azure Static Web Apps** | Provides global availability, native SSL, and CI/CD via GitHub Actions. |
| **Auth** | **Firebase Authentication** | Handles secure user management (Email/Password & Anonymous login). |
| **Database** | **Cloud Firestore (NoSQL)** | Stores wardrobe inventory with complex metadata (warmth_rating, formal_rating, etc.). |
| **APIs** | **Weather API & Outlook** | External data sources for context awareness. |

### Architecture Diagram
*(Add your diagram screenshot here, e.g., `![Architecture](./images/architecture.png)`)*

### Data Flow
1.  **Context:** App fetches Weather & Schedule.
2.  **Filter:** AI filters wardrobe by Weather (Warmth Rating).
3.  **Refine:** AI filters by Schedule (Formal Rating).
4.  **Rank:** Items ranked by "Last Worn Date".
5.  **Output:** Optimal Outfit Recommendation.

---

## 🚀 Getting Started

To run this project locally:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/iosifidis/outfit-buddy.git
    cd outfit-buddy
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Set up Environment Variables:**
    Create a `.env.local` file and add your Firebase and Azure API keys.

4.  **Run the development server:**
    ```bash
    npm run dev
    ```

5.  **Open your browser:**
    Navigate to `http://localhost:3000`.

---

## 👥 Team (Outfit Buddies - Team 2)

*   **Efstathios Ioasifidis**
*   **Evangelia Tsioumani**
*   **Dimitris Topalidis**
*   **Christos Kopsahilis**
*   **Nalmpanti Effrosyni**

---

*Project created: December 7, 2025*
