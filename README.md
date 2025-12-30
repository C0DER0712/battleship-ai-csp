# Adaptive Battleship AI using CSP and Heuristic Search Strategies

An intelligent Battleship game agent that uses **Constraint Satisfaction Problems (CSP)** and **heuristic search strategies** to make strategic decisions for ship placement and targeting.

## 📌 Project Overview

This project implements an AI-powered Battleship game that demonstrates classical AI techniques applied to strategic gameplay. The AI mimics human-like decision-making by employing constraint satisfaction for ship placement and adaptive targeting strategies based on game state knowledge.

## 👥 Authors

- **Syed Farhan Syed Sathik Basha** (CS23B2039)
- **Mohamed Amjad** (CS23B2013) (Myself)

## 🎯 Objectives

The Battleship AI is designed to:
- Place ships validly and efficiently using CSP
- Make intelligent guesses using knowledge from previous hits and misses
- Utilize heuristics to efficiently target and sink ships
- Demonstrate strategic reasoning and pattern recognition in gameplay

## 🎮 Game Environment

- **Grid Size**: 10x10 per player
- **Ships**: 
  - Carrier (5 cells)
  - Battleship (4 cells)
  - Cruiser (3 cells)
  - Submarine (3 cells)
  - Destroyer (2 cells)
- **Rules**: Ships cannot overlap and must remain within grid boundaries

## 🧠 AI Concepts & Techniques

### 1. Constraint Satisfaction Problems (CSP)
- **Ship Placement**: Each ship is modeled as a CSP with:
  - **Variables**: Ships
  - **Domains**: Valid horizontal and vertical placements
  - **Constraints**: No overlapping, within grid boundaries
- **Targeting**: Determines valid ship placements by pruning impossible configurations

### 2. Heuristic Targeting Strategy
The AI uses multiple intelligent strategies for shot selection:

- **Adjacency Check**: After a hit, evaluates adjacent cells for follow-up shots
- **Line Extension**: Extends aligned hits in horizontal/vertical directions
- **CSP Targeting**: Calculates valid placements based on remaining ship sizes
- **Heuristic Move**: For unexplored areas, calculates placement probabilities for each cell based on remaining ships

### 3. Stateful Memory
The AI maintains complete game state knowledge:
- All shots fired (hits and misses)
- Ships that have been sunk
- Active targeting patterns
- Valid remaining ship configurations

### 4. Sink Confirmation
Ships are only marked as sunk when all expected positions based on the hit pattern are verified.

## 🛠️ Implementation

- **Language**: Python
- **Environment**: Jupyter Notebook (Google Colab compatible)
- **Game Modes**: 
  - AI vs AI
  - Player vs AI with interactive gameplay
- **Visualization**: Displays both full board (true placements) and shots board (discovered cells)

## 📊 Results

The AI demonstrates significant performance improvements over random strategies:

- **Comparative Analysis**: CSP + Heuristic approach requires fewer guesses than random targeting
- **Avoids repeated incorrect guesses**
- **Targets effectively around confirmed hits**
- **Efficiently sinks ships using adjacent cell traversal**
- **Maintains legal ship placement throughout the game**

## 🚀 Usage

### Running the Game

```python
# Choose game mode:
# 1. AI vs AI
# 2. Player vs AI

# The game displays:
# - Initial ship placements
# - Turn-by-turn gameplay
# - Full board (actual ship positions)
# - Shots board (discovered information)
```

### Game Flow

1. Ships are placed using CSP
2. Players/AI take turns firing at opponent's grid
3. AI uses heuristic strategies to decide next shot
4. Game continues until all ships of one player are sunk

## 📁 Project Structure

- `AI_PROJECT.ipynb` - Main implementation notebook
- `AI_project-report.pdf` - Detailed project report

## 🎓 Key Learnings

This project successfully demonstrates:
- Application of classical AI concepts (CSP, heuristics) to game strategy
- Adaptive decision-making based on incomplete information
- Pattern recognition and strategic reasoning
- Performance comparison between intelligent and random strategies

## 📝 Conclusion

By combining **Constraint Satisfaction Problems** for ship placement and **adaptive targeting strategies** with stateful memory, this AI agent successfully mimics human-like strategic thinking in the Battleship game environment, achieving superior performance over baseline random strategies.

---


