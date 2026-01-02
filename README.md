# Tokyo Flight

A browser-based endless runner game built with p5.js, featuring responsive design, Arduino sensor integration, and a collection of unlockable airplane skins. Navigate through the skies, collect stars, avoid bombs, and unlock new airplane designs as you progress!

![Tokyo Flight](https://img.shields.io/badge/p5.js-1.11.11-orange) ![License](https://img.shields.io/badge/license-MIT-blue)

## 🎬 Demo Videos & Documentation

**Watch the game in action!** Check out demo videos and project documentation:

📹 **[View Demo Videos & Schematics on Google Drive](https://drive.google.com/drive/folders/1JJhlXQudq4Fsjmf-fyrTgjc6DV5u6rEX?usp=sharing)**

The folder includes:
- **Demo Videos**: Multiple gameplay demonstrations showcasing different features
- **Circuit Schematics**: Digital and analog circuit diagrams for Arduino integration
- **Testing Footage**: Development and testing process videos

### Physical Model

![3D-Printed Airplane Model with Arduino Integration](IMG_5875%202.JPG)

*3D-printed airplane model with integrated Arduino components (LEDs, buttons, and accelerometer) for motion-based game controls*

## 🎮 Game Overview

Tokyo Flight is an interactive side-scrolling game where players control an airplane through a dynamic sky environment. The game combines classic arcade gameplay with modern web technologies and hardware integration.

### Key Features

- **Endless Runner Gameplay**: Navigate your airplane through an ever-changing sky, collecting stars for points while avoiding bombs
- **Boost System**: Use boost energy to speed up and gain advantages, with a strategic energy management system
- **Progressive Difficulty**: Game difficulty increases over time, providing an escalating challenge
- **Heart System**: Collect heart items to restore health and extend your gameplay
- **Skin Collection**: Unlock new airplane skins by achieving higher scores (unlock a new skin every 100 points)
- **Leaderboard**: Track your top 10 scores with local storage persistence
- **Arduino Integration**: Optional accelerometer sensor support for motion-based controls via WebSerial API
- **Responsive Design**: Scales beautifully across different screen sizes
- **Background Music**: Immersive audio experience with Studio Ghibli-inspired music tracks
- **Multiple Game Modes**: Landing page, instructions, gameplay, collection viewer, and story mode

## 🛠️ Technologies Used

- **p5.js** (v1.11.11) - Creative coding framework for graphics and interactivity
- **p5.sound** - Audio library for background music and sound effects
- **p5.webserial** - WebSerial API integration for Arduino communication
- **HTML5/CSS3** - Structure and styling
- **JavaScript (ES6+)** - Game logic and state management
- **LocalStorage API** - Persistent data storage for scores and unlocked content
- **Arduino** - Optional hardware integration for motion controls

## 📁 Project Structure

```
tokyo-flight/
├── index.html          # Main HTML file
├── sketch.js           # Main game logic and state management
├── Plane.js            # Airplane class with skin system
├── Star.js             # Collectible star items
├── Bomb.js             # Obstacle bombs
├── HeartItem.js        # Health restoration items
├── Cloud.js            # Background cloud elements
├── planes.png          # Sprite sheet for airplane skins
├── studio_ghibli.mp3   # Menu background music
├── spirited_away1.mp3  # Gameplay background music
├── style.css           # Styling
└── arduino_code.ino    # Arduino code for sensor integration
```

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, or Safari)
- A local web server (for audio file loading - required by p5.js)
- Optional: Arduino board with accelerometer sensor for motion controls

### Installation

1. Clone or download this repository
2. Set up a local web server. You can use one of the following methods:

   **Using Python:**
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```

   **Using Node.js (http-server):**
   ```bash
   npx http-server -p 8000
   ```

   **Using VS Code:**
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

3. Open your browser and navigate to `http://localhost:8000`

### Arduino Setup (Optional)

1. Upload `arduino_code.ino` to your Arduino board
2. Connect the accelerometer sensor according to the code specifications
3. In the game, click the "Connect" button to establish WebSerial connection
4. Select your Arduino port from the browser's serial port selection

## 🎯 How to Play

### Controls

- **Arrow Keys (↑/↓)**: Move the airplane up and down
- **Spacebar**: Activate boost (consumes boost energy)
- **Arduino Sensor** (if connected): Tilt the sensor to control the airplane's vertical position

### Gameplay Mechanics

- **Stars**: Collect yellow stars to increase your score
- **Bombs**: Avoid red bombs - they reduce your health
- **Hearts**: Collect pink heart items to restore health
- **Boost Energy**: Limited resource that recharges over time. Use it strategically!
- **Difficulty Scaling**: Game speed and obstacle frequency increase as you play longer
- **Skin Unlocking**: Unlock new airplane skins every 100 points

### Game States

- **LANDING**: Main menu with name input and navigation options
- **INSTRUCTIONS**: Game tutorial and controls
- **PLAYING**: Active gameplay
- **GAMEOVER**: End screen with score and leaderboard
- **COLLECTION_PAGE**: View all unlocked airplane skins
- **STORY_PAGE**: Game narrative and background

## 🎨 Features in Detail

### Responsive Design
The game automatically scales to fit different screen sizes while maintaining aspect ratio, ensuring a consistent experience across devices.

### Skin Collection System
- Start with one default airplane skin
- Unlock new skins by achieving higher scores
- View your collection in the Collection page
- Skins are saved locally and persist across sessions

### Leaderboard
- Tracks top 10 scores with player names
- Automatically saves to browser's local storage
- Displays date of achievement
- Sorted by highest score first

### Audio System
- Dynamic music switching between menu and gameplay
- Smooth fade transitions between tracks
- Volume control and looping

### Arduino Integration
- Real-time accelerometer data reading
- Motion-based airplane control
- WebSerial API for browser-Arduino communication
- Fallback to keyboard controls if sensor is not connected

## 🏗️ Architecture

The game follows an object-oriented design pattern with separate classes for each game element:

- **Plane**: Player-controlled airplane with skin system and collision detection
- **Star**: Collectible items that increase score
- **Bomb**: Obstacles that damage the player
- **HeartItem**: Health restoration items
- **Cloud**: Background decorative elements

State management is handled through a centralized `gameState` variable, with dedicated functions for each state's rendering and logic.

## 📊 Performance Optimizations

- Efficient collision detection using distance calculations
- Object pooling for game entities (stars, bombs, hearts)
- Responsive scaling calculations cached and reused
- Local storage operations optimized to prevent performance issues

## 🔮 Future Enhancements

Potential improvements for future versions:
- Online multiplayer leaderboard
- Additional power-ups and special items
- More diverse obstacle types
- Enhanced visual effects and animations
- Mobile touch controls
- Achievement system
- Sound effect library expansion

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

Created as a portfolio project demonstrating skills in:
- Creative coding with p5.js
- Game development and design
- Web APIs (WebSerial, LocalStorage)
- Hardware integration (Arduino)
- Responsive web design
- State management
- Object-oriented programming

## 🙏 Acknowledgments

- p5.js community for the excellent creative coding framework
- Studio Ghibli for musical inspiration
- All contributors to the open-source libraries used in this project

---

**Enjoy flying through the Tokyo skies!** ✈️✨

