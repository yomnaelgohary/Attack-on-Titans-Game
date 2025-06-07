
# Attack on Titan: Utopia 🏰👹

![Java](https://img.shields.io/badge/Java-17%2B-blue)  
![JavaFX](https://img.shields.io/badge/JavaFX-20-FF7F50)  
![License](https://img.shields.io/badge/License-MIT-green)  
![Pattern](https://img.shields.io/badge/Pattern-MVC-brightgreen)

A strategic tower defense game inspired by *Attack on Titan*, developed in JavaFX for **CSEN 401** at the German University in Cairo.

---

## Table of Contents
- [Game Overview](#game-overview)  
- [Features](#features)  
- [Technical Implementation](#technical-implementation)  
- [How to Run](#how-to-run)  
- [Project Structure](#project-structure)  
- [Team](#team)  

---

## Game Overview

Defend your fortress walls against waves of Titans! Choose between **Easy (3 lanes)** and **Hard (5 lanes)** difficulty modes, deploy strategic weapons, and survive through three escalating battle phases:

- **Titan Types**: Pure, Abnormal, Armored, and Colossal Titans — each with unique abilities (double attacks, damage resistance, etc.)
- **Battle Phases**: EARLY, INTENSE, and GRUMBLING phases, with increasing Titan difficulty and numbers
- **JavaFX GUI**: Interactive, real-time display of lanes, walls, resources, and weapons

---

## Features

### Core Game Engine

- **Titan System**  
  - Four Titan classes with distinct behaviors and strengths  
- **Weapon System**  
  | Weapon Type      | Attack Pattern           |  
  |------------------|--------------------------|  
  | Piercing Cannon  | Hits closest 5 Titans     |  
  | Sniper Cannon    | Single target             |  
  | VolleySpread     | Area-of-effect            |  
  | Wall Trap        | Defensive utility         |  

- **Battle Progression**  
  - Phased difficulty with adaptive gameplay mechanics  
- **Exception Handling**  
  - Custom exceptions for invalid actions (e.g., insufficient resources)

### JavaFX GUI

- **Mode Selection**: Easy or Hard with visual cues  
- **Dynamic Gameplay Display**:  
  - Lane health and danger levels  
  - Visual differentiation of Titans and weapons  
  - Turn, phase, and resource tracking  
- **User Interaction**:  
  - Weapon purchasing system  
  - Lane and target selection  
  - Real-time notifications and error handling  

---

## Technical Implementation

- **OOP Architecture**: 15+ classes with strict inheritance and encapsulation  
- **Design Patterns**: Model-View-Controller (MVC), Factory, Observer  
- **Data Management**: Game assets loaded via CSV files for easy updates  
- **Custom Exceptions**: Enhance game rule enforcement and user feedback  

```java
// Example: Custom exception for insufficient resources
public class InsufficientResourcesException extends GameActionException {
    public InsufficientResourcesException(int resources) {
        super("Not enough resources! Available: " + resources);
    }
}
```

---

## How to Run

1. Ensure **Java 17+** and **JavaFX 20** are installed.  
2. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/attack-on-titan-utopia.git
   ```  
3. Build and run the project using your preferred IDE (e.g., IntelliJ, Eclipse) or with Maven/Gradle.  
4. Launch the game and select your mode to start defending!

---

## Project Structure

- `model/` — Core game logic and entities (Titans, weapons, phases)  
- `view/` — JavaFX UI components and screens  
- `controller/` — Input handlers and game flow management  
- `exceptions/` — Custom exception classes  
- `resources/` — CSV files and assets for Titans and weapons  

---

## Team

- **Yomna Khaled Elgohary** 
- **Mennatallah Mohamed Eldafrawy**
- **Shahd Khaled Abuelwafa** 
