# 🌍 GeoGame: Where Are We?
**GMT 458 – Web GIS - Assignment 2**

This project is an interactive geography guessing game developed for the GMT 458 course. It utilizes the **OpenLayers**, **Chart.js**, and **GSAP** libraries to create a polished, data-driven web application.

[![Live Demo Button](https://img.shields.io/badge/Live_Demo-Play_Now!-brightgreen?style=for-the-badge&logo=github-pages)](https://gmt-458-web-gis.github.io/geogame-mustafabtw/)

---

### 🎮 Game Layout and Interface

The game is built on a modern, dark theme. The user interface is designed to be minimalist and animated, ensuring an immersive experience without distracting the player.

| Intro Screen | Main Menu | Game Screen (with Hint) | Settings Panel | Game Over (Score) |
| :---: | :---: | :---: | :---: | :---: |
| <img width="1860" height="830" alt="intro_ss" src="https://github.com/user-attachments/assets/72941f20-3df3-4a22-8b26-d7e5a4c6a91c" /> | <img width="1857" height="881" alt="main_menu_ss" src="https://github.com/user-attachments/assets/a2a52410-62cd-4b65-88c3-5fff6aca1eb4" /> | <img width="1862" height="878" alt="game_ss" src="https://github.com/user-attachments/assets/e5d76f28-388c-4a79-b2bf-a7f9e9109ee0" /> | <img width="1867" height="897" alt="settings_ss" src="https://github.com/user-attachments/assets/6ad40a87-cf76-411f-b2b9-6e8a8b7a73af" /> | <img width="1867" height="893" alt="scoreboard_ss" src="https://github.com/user-attachments/assets/ad6e234d-aa65-405d-83bc-1db81f16871f" /> |

---

### ✨ Key Features

* **Dynamic Map Layers:** Players can instantly switch between three different map styles from the Settings menu, powered by OpenLayers tile layers:
    * **Satellite:** A realistic, high-resolution satellite view.
    * **Dark Mode:** A stylized, low-light map for comfortable night-time play.
    * **Light Mode:** A clean and minimal daytime map.
* **Interactive Hints:** A token-based system allows players to spend earned currency on two types of hints: visual (Food) or abstract (Flag Colors).
* **Autocomplete Search:** A custom-built suggestion box filters through all world capitals as the user types, improving usability.
* **Performance Analytics:** At the end of each game, a **Chart.js** doughnut graph provides instant visual feedback on the player's correct-to-wrong answer ratio.
* **Polished Animations:** Using **GSAP**, the game features a cinematic intro, smooth screen transitions, and dynamic flight animations that draw the route between capitals.

---

### 🎯 Project Requirements 

#### 1. How the game will progress
The game is a time- and life-based challenge.
* **Time:** The user starts with **2 minutes (120 seconds)**.
* **Bonus Time:** Each correct guess awards the player **+10 seconds**.
* **Difficulty:** The 25 questions are shuffled at the start of each session, ensuring high replayability.
* **Scoring:** Each correct answer awards +100 Points and +5 Tokens (for the hint system).

#### 2. How many questions will there be
* The game's database (in `oyun.js` > `gameData`) contains a total of **25 unique capitals**.

#### 3. How many lives does a user have
* The user starts the game with **3 lives** (💛💛💛). One life is lost for each incorrect guess.

---

### 🛠️ Technologies & JS Libraries Used

This project was built using modern web technologies and includes advanced libraries as specified in the assignment for bonus consideration.

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

* **OpenLayers:**
    * Used for the core map infrastructure, view projection, and tile layer management (Satellite, Dark, Light).
    * Handles the vector layer animations (LineString) to draw the flight path between destinations.

* **Chart.js (Bonus Library):**
    * Used on the game summary screen (`summary-screen`) to visualize the player's performance.

* **GSAP (GreenSock Animation Platform):**
    * Used for all fluid UI animations, including the intro, screen fades, pop-up modals, and coordinating the flight animation.
