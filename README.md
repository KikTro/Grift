# GRIFT

**Mechanical Logic Engine**

> “Simple, yet not simple. Takes minutes to master, hours to think deeply.”

##  About The Project

**GRIFT** is a logic-based strategy board game that blends the intensity of Chess with mechanical rotation physics. Unlike static board games, the board in Grift is alive—after every round of moves, the concentric rings of the board rotate counter-clockwise, shifting the entire landscape of the game.

The aesthetic is inspired by dark-mode strategy interfaces and retro-modern tech, featuring a **"Tech Orange" (#fa471f)** and **"Matte Grey"** palette.

##  Key Features

*   **Mechanical Rotation Core:** The board consists of concentric tracks that rotate after every turn.
*   **Dual Game Modes:**
    *   **Local Play:** Pass-and-play on a single device.
    *   **Online Multiplayer:** Host/Join lobbies with real-time syncing via Firebase.
*   **Progressive Web App (PWA):** Installable on mobile devices for a native, full-screen experience.
*   **Audio Engine:** Procedurally generated sound effects for satisfying tactile feedback (clicks, slides, thuds).
*   **Adaptive Logic:** Configure board complexity (2 to 5 rings) and time controls.

##  How to Play

**Objective:** Connect 4 (or more) pieces in a straight line—horizontally, vertically, or diagonally.

*Note: The number of pieces required to win increases with the number of rings (e.g., 2 rings = Connect 4, 3 rings = Connect 5).*

### The Sequence

1.  **Phase 1:** White (Grey) places a piece.
2.  **Phase 2:** Black (Orange) places a piece.
3.  **Phase 3:** The player who moved second presses the **Center Button**.

### The Twist
Pressing the center button triggers the **Mechanical Rotation**. All rings rotate one step counter-clockwise.

**Strategy:** You must not aim for where the line is now, but where it will be *after* the rotation.

##  Tech Stack

*   **Frontend Framework:** React (Vite)
*   **Styling:** Tailwind CSS
*   **Icons:** Lucide React
*   **Backend / Realtime:** Firebase (Firestore & Auth)
*   **Audio:** Web Audio API (No external assets, purely synthesized)
 
##  Getting Started

Follow these instructions to set up the project locally on your machine.

### Prerequisites

*   Node.js (v16 or higher)
*   npm (Node Package Manager)

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Grift.git
    cd Grift
    ```

2.  Install dependencies:
    ```sh
    npm install
    ```
    *(Note: If you encounter PostCSS errors, ensure you are using a compatible Tailwind version: `npm install -D tailwindcss@3.4.17 postcss autoprefixer`)*

3.  Configure Firebase:
    *   Create a project at [Firebase Console](https://console.firebase.google.com/).
    *   Enable **Authentication** (Anonymous Sign-in).
    *   Enable **Firestore Database** (Start in Test Mode).
    *   Copy your web app configuration keys.
    *   Open `src/App.jsx` and replace the placeholder `firebaseConfig` object with your own keys.

4.  Run the development server:
    ```sh
    npm run dev
    ```
    Open the link shown in your terminal (usually `http://localhost:5173`).

## 🌍 Deployment (GitHub Pages)

This project is configured for deployment to GitHub Pages.

1.  **Update Configuration:**
    *   In `vite.config.js`, ensure the `base` property matches your repository name:
        ```js
        base: '/Grift/',
        ```
    *   In `package.json`, add/update the `homepage` field:
        ```json
        "homepage": "https://<your-username>.github.io/Grift"
        ```

2.  **Deploy:**
    Run the deployment script:
    ```sh
    npm run deploy
    ```
    This builds the project to the `dist` folder and pushes it to the `gh-pages` branch.

## Credits

Built by: **Krishnendu Halder**, **KikTro**

> “Control the orbit, control the game.”
