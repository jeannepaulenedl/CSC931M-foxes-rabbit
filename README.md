# Predator-Prey Ecosystem Simulation

## Overview

This NetLogo simulation models a predator-prey ecosystem, consisting of two primary agents: **foxes** (predators) and **rabbits** (prey), as well as grass, which serves as food for the rabbits. The ecosystem follows a set of behavioral rules to explore the dynamics of predator-prey relationships and population fluctuations over time.

## Simulation Components

### 1. **Rabbits** (Prey):
   - **Movement**: Rabbits move randomly and take smaller steps compared to foxes.
   - **Energy**: Rabbits lose energy every tick and gain energy by eating grass on green patches.
   - **Reproduction**: Rabbits reproduce when their energy exceeds a threshold, splitting their energy with the offspring.
   - **Death**: Rabbits die either from old age or if their energy falls below zero.

### 2. **Foxes** (Predators):
   - **Movement**: Foxes move in relatively straight paths to chase prey, taking larger steps.
   - **Hunting**: Foxes chase rabbits closer to them / within a **0.5-unit radius**. Once a rabbit is within this range, the fox gains energy by consuming the rabbit, which dies as a result.
   - **Energy**: Foxes lose energy every tick and gain energy by consuming rabbits.
   - **Reproduction**: Foxes reproduce when their energy exceeds a threshold, splitting energy with their offspring.
   - **Death**: Foxes die either from old age or if their energy falls below zero.

### 3. **Grass**:
   - **Regrowth**: Grass grows on patches with a regrowth time. Rabbits consume grass, turning patches brown, which then regenerate after the countdown reaches zero.

## Model Controls

- **Initial Number of Rabbits**: Slider to set the number of rabbits at the start of the simulation (0-100).
- **Initial Number of Foxes**: Slider to set the number of foxes at the start of the simulation (0-100).
- **Foxes Gain from Food**: Slider to adjust the energy foxes gain by eating rabbits (default: 25).
- **Rabbits Gain from Food**: Slider to adjust the energy rabbits gain by eating grass (default: 5).
- **Grass Regrowth Time**: Slider to control the time it takes for grass to regrow on brown patches (default: 25).
- **Foxes Reproduce Rate**: Slider to adjust the reproduction rate of foxes (0%-100%, default: 5%).
- **Rabbits Reproduce Rate**: Slider to adjust the reproduction rate of rabbits (0%-100%, default: 10%).
- **Show Energy**: Toggle to display the energy of rabbits and foxes.
- **Limited Mode**: Toggle to limit the simulation to 500 ticks or run indefinitely.

## How to Run the Model

1. Click the **Setup** button to initialize the simulation.
2. Use the sliders to configure initial population sizes and other parameters.
3. Click the **Go** button to start the simulation.

The model will stop automatically if any of the populations (foxes, rabbits, or grass) goes extinct, or if it is run in limited mode and reaches 500 ticks.

---

