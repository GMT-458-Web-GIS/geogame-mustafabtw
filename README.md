# 🌍 GeoGame: Where Are We?
**GMT 458 – Web GIS - Assignment 2**

This project is an interactive geography guessing game developed for the GMT 458 course. It utilizes the **OpenLayers**, **Chart.js**, and **GSAP** libraries to create a polished, data-driven web application.

[![Live Demo Button](https://img.shields.io/badge/Live_Demo-Play_Now!-brightgreen?style=for-the-badge&logo=github-pages)](https://gmt-458-web-gis.github.io/geogame-mustafabtw/)

---

### 🎮 Game Layout and Interface

The game is built on a modern, dark theme. The user interface is designed to be minimalist and animated, ensuring an immersive experience without distracting the player.

| Intro Screen | Main Menu | Game Screen (with Hint) | Settings Panel | Game Over (Score) |
| :---: | :---: | :---: | :---: | :---: |
| <img width="1860" height="830" alt="intro_ss" src="https://github.com/user-attachments/assets/72941f20-3df3-4a22-8b26-d7e5a4c6a91c" /> | <img width="1857" height="881" alt="main_menu_ss" src="https://github.com/user-attachments/assets/a2a52410-62cd-4b65-88c3-5fff6aca1eb4" /> | <img width="1862" height="878" alt="game_ss" src="https://github.com/user-attachments/assets/e5d76f28-388c-4a79-b2bf-a7f9e9109ee0" /> | **[Drag & Drop Settings SS Here]** | <img width="1867" height="893" alt="scoreboard_ss" src="https://github.com/user-attachments/assets/ad6e234d-aa65-405d-83bc-1db81f16871f" /> |

---

### 🎯 Project Requirements & Mechanics (Assignment Part 1)

This section details the game's mechanics and answers the questions required for the 17 November design phase of the assignment.

#### 1. How the game will progress
The game is a time- and life-based challenge.
* **Time:** The user starts with **2 minutes (120 seconds)**.
* **Bonus Time:** Each correct guess awards the player **+10 seconds**.
* **Difficulty:** The questions (from the `gameData` array) are shuffled at the start of each session, ensuring a different experience every time.
* **Scoring:** Each correct answer awards +100 Points and +5 Tokens.

#### 2. How many questions will there be
* The game's database (in `oyun.js` > `gameData`) contains a total of **25 unique capitals**.

#### 3. How many lives does a user have
* The user starts the game with **3 lives** (💛💛💛).
* One life is lost for each incorrect guess.
* The game ends when the user runs out of lives or time.

#### 4. Hint System
* Players can spend tokens (earned from correct guesses) to receive hints.
* **Food Hint (10 Tokens):** Shows a visual of a famous dish from the capital's country.
* **Flag Colors Hint (10 Tokens):** Shows the main colors of the country's flag.

---

### 🛠️ Technologies & JS Libraries Used

This project was built using modern web technologies and includes advanced libraries as specified in the assignment for bonus consideration.

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

* **OpenLayers:**
    * Used for the core map infrastructure, tile layer management (Dark, Light, Satellite), and map rendering.
    * Handles the flight animation (Vector Layer, LineString) to the next destination after a correct guess.

* **Chart.js (Bonus Library):**
    * Used on the game summary screen (`summary-screen`) to visualize the player's performance.
    * It displays a **Doughnut chart** comparing the number of correct guesses vs. wrong attempts.

* **GSAP (GreenSock Animation Platform):**
    * Used for all fluid UI animations that enhance the game's "polish" and user experience.
    * Manages the game intro sequence, screen transitions (fade-in/out), pop-up modals, and the timing of the flight animation.
