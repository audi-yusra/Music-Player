# Music Player

This project is a simple yet functional **Music Player** built using Python and the `pygame` library. It allows users to play, pause, stop, and navigate through a playlist of audio files. The player provides a user-friendly interface for managing and listening to music.

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Code Explanation](#code-explanation)

---

## Introduction

The **Music Player** is a Python-based application designed to provide a seamless music playback experience. It supports basic audio controls such as play, pause, stop, next, and previous. The player is built using the `pygame` library, which is widely used for multimedia applications in Python.

---

## Features

- **Play/Pause**: Start or pause the current track.
- **Stop**: Stop the playback entirely.
- **Next/Previous Track**: Navigate through the playlist.
- **Volume Control**: Adjust the volume of the playback.
- **Playlist Management**: Load and manage a list of audio files.
- **User-Friendly Interface**: Simple and intuitive controls.

---

## Requirements

- Python 3.x
- Pygame library

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/audi-yusra/Music-Player.git
   cd Music-Player
   ```

2. Install the required dependencies:
   ```bash
   pip install pygame
   ```

---

## Usage

1. Run the script:
   ```bash
   python music_player.py
   ```

2. Use the following controls to interact with the music player:
   - **Play/Pause**: Spacebar or click the play/pause button.
   - **Stop**: Click the stop button.
   - **Next Track**: Click the next button.
   - **Previous Track**: Click the previous button.
   - **Volume Control**: Use the volume slider.

3. Load your music files into the `music` folder or specify the path to your audio files in the code.

---

## Code Explanation

### Key Components

1. **Music Player Class**:
   - Manages the playback of audio files.
   - Handles play, pause, stop, next, and previous functionalities.

   ```python
   class MusicPlayer:
       def __init__(self):
           pygame.mixer.init()
           self.playlist = []
           self.current_track = 0
           self.playing = False
   ```

2. **Playlist Management**:
   - Loads audio files from a specified directory.
   - Allows navigation through the playlist.

   ```python
   def load_playlist(self, directory):
       for file in os.listdir(directory):
           if file.endswith(".mp3"):
               self.playlist.append(os.path.join(directory, file))
   ```

3. **Audio Controls**:
   - Provides functions to play, pause, stop, and skip tracks.

   ```python
   def play(self):
       if not self.playing:
           pygame.mixer.music.load(self.playlist[self.current_track])
           pygame.mixer.music.play()
           self.playing = True

   def pause(self):
       if self.playing:
           pygame.mixer.music.pause()
           self.playing = False
   ```

4. **User Interface**:
   - Uses `pygame` to create a simple graphical interface for the music player.

   ```python
   def draw_buttons(self):
       # Draw play, pause, stop, next, and previous buttons
       pass
   ```

---
