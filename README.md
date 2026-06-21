# Bone Deep Bad Decisions - Choice-Based Adventure Game

A terminal-based dark dungeon escape game built in Python. This project takes branching narrative design and applies state-tracking logic to ensure that every player choice dynamically changes gameplay pathways, inventory items, and terminal endings.

> "Every choice leaves a mark."

---

## 🛠️ Tech Stack & Concepts
* **Language:** Python 3
* **Core Concepts:** Global State Management, Conditional Branching (if-elif-else), State-Driven Game Loops, and the `random` Module for Dynamic Combat Scaling.

---

## 🚀 Key Features

The game features an interactive story structure with multiple branches and dynamic game mechanics:

* **State Initialization:** Safely manages player attributes (Health and Attack stats) alongside a multi-item Boolean inventory engine.
* **Dynamic Story Branching:** Splitting pathways (e.g., East Armory vs. West Hallway, Left Bone Pit vs. Right Spider Nest) provide unique environments, custom dialog trees, and distinct items.
* **Persistent Choice Tracking:** Early interactions affect future rooms. For example, waving at a skeleton or answering a talking spider's riddle changes the traps and keys available later in the game.
* **Active Combat System:** Turn-based battle mechanics allow players to Attack or Defend, processing mathematical equations to update real-time enemy metrics.
* **Randomized Success Engine:** Uses Python's `random` tracking module to calculate a 30% dodge probability during normal fights, and a 50/50 success split during high-risk brute force escapes.
* **Multiple Ending Matrix:** Evaluates inventory items and health thresholds upon reaching the final door to award 4 distinct endings (Good Ending, Alternate Strength Ending, or two different Bad Endings).

---

## 🧠 Defensive Programming & Engineering Insights

This section highlights the design choices made to ensure the application remains stable, readable, and structured for classroom concepts.

### 🛡️ Defensive Architecture (Crash Prevention)
* **Fallback Input Handling:** If a player inputs an invalid command or unexpected character string, the conditional blocks catch the outlier, prompt an in-universe penalty or warning message, and gracefully loop the user back to make a valid choice.
* **Encapsulated Memory Resets:** Invoking `original_stats()` inside the main menu loop flushes old runtime data out of memory, resetting global variables to factory defaults so replays work cleanly without script restarts.

### ⚙️ Engineering Design (Data Handling)
* **Global State Architecture:** Leverages organized `global` variable definitions to sync inventory arrays and state markers across separate modular function blocks.
* **Clean Functional Modularization:** Every major room, encounter, and fight loop is broken down into its own standalone Python function, simplifying script expansion and keeping development organized.

---

## 💻 How to Run

This game uses core native Python tools and requires absolutely no third-party package dependencies.

### Prerequisites
* Python 3 installed on your local computer.

### Steps

1. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/Mehreen-Mitha/Choice-Based-Narrative-Game-PythonPrototype.git
```

2. Navigate to the Project Folder

```bash
cd Choice-Based-Narrative-Game-PythonPrototype
```

3. Compile and Run

Depending on your project structure, use the appropriate commands. For example:

```bash
# If using javac
javac -d bin src/*.java
java -cp bin MainClassName
```

> **Note:** If you are using an IDE such as IntelliJ IDEA, Eclipse, or VS Code, you can simply select **Open Project** and choose the cloned folder. The IDE will automatically detect and configure the source code.
