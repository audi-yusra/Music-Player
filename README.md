# Music Player Web Application

This project is a **Music Player** web application built using HTML, CSS, and JavaScript. It provides a sleek and user-friendly interface for playing music tracks, with features like play/pause, next/previous track navigation, and a progress bar for tracking playback. The application dynamically updates the background and album cover based on the currently playing song.

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Code Explanation](#code-explanation)

---

## Introduction

The **Music Player** is a web-based application designed to provide a seamless music playback experience. It allows users to play, pause, and navigate through a playlist of songs. The application dynamically updates the album cover and background image based on the currently playing track, creating an immersive experience.

---

## Features

- **Play/Pause**: Start or pause the current track.
- **Next/Previous Track**: Navigate through the playlist.
- **Dynamic Background**: The background image changes based on the currently playing song.
- **Progress Bar**: Track the playback progress and seek to a specific point in the song.
- **Responsive Design**: Works seamlessly on both desktop and mobile devices.

---

## Requirements

- A modern web browser (Chrome, Firefox, Safari, Edge, etc.).
- No additional installations are required as the application runs entirely in the browser.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/audi-yusra/Music-Player.git
   cd Music-Player
   ```

2. Open the `index.html` file in your browser:
   ```bash
   open index.html
   ```

---

## Usage

1. Open the application in your browser.
2. Use the following controls to interact with the music player:
   - **Play/Pause**: Click the play/pause button.
   - **Next Track**: Click the next button.
   - **Previous Track**: Click the previous button.
   - **Progress Bar**: Click anywhere on the progress bar to seek to a specific point in the song.

3. The background and album cover will automatically update based on the currently playing song.

---

## Code Explanation

### Key Components

1. **HTML Structure**:
   - The `index.html` file defines the structure of the music player, including the album cover, song title, artist name, progress bar, and control buttons.

   ```html
   <div class="container">
       <div class="player-img">
           <img src="" class="active" id="cover">
       </div>
       <h2 id="music-title"></h2>
       <h3 id="music-artist"></h3>
       <div class="player-progress" id="player-progress">
           <div class="progress" id="progress"></div>
           <div class="music-duration">
               <span id="current-time">0:00</span>
               <span id="duration">0:00</span>
           </div>
       </div>
       <div class="player-controls">
           <i class="fa-solid fa-backward" title="Previous" id="prev"></i>
           <i class="fa-solid fa-play play-button" title="Play" id="play"></i>
           <i class="fa-solid fa-forward" title="Next" id="next"></i>
       </div>
   </div>
   ```

2. **CSS Styling**:
   - The `style.css` file provides the styling for the music player, including the layout, colors, and animations.

   ```css
   .container {
       background-color: #e7e7e7;
       height: 500px;
       width: 400px;
       border-radius: 20px;
       box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
       transition: all 0.5s ease;
   }

   .player-img img.active {
       width: 100%;
       height: 100%;
       transition: all 0.5s;
       opacity: 1;
   }
   ```

3. **JavaScript Functionality**:
   - The `index.js` file handles the logic for playing, pausing, and navigating through songs, as well as updating the progress bar and background image.

   ```javascript
   const music = new Audio();

   const songs = [
       {
           path: 'assets/1.mp3',
           displayName: 'Falling in Love',
           cover: 'assets/1.jpg',
           artist: 'Salman Khan',
       },
       {
           path: 'assets/2.mp3',
           displayName: 'Butter',
           cover: 'assets/2.jpg',
           artist: 'BTS',
       },
       {
           path: 'assets/3.mp3',
           displayName: 'Bade Achhe Lagte Hain',
           cover: 'assets/3.jpg',
           artist: 'Shreya Ghoshal',
       }
   ];

   function togglePlay() {
       if (isPlaying) {
           pauseMusic();
       } else {
           playMusic();
       }
   }
   ```

---
