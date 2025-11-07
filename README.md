# NFL Player Trajectory Prediction

## Project Description
Developed a predictive model to forecast NFL player trajectories during pass plays using 
pre-throw tracking data, targeted receiver info, and ball landing location. 
Leveraged sequence modeling and interaction-aware architectures to minimize RMSE between 
predicted and actual movements.

---

## Overview
This project focuses on predicting the movement of NFL players during pass plays after the ball 
is thrown. Using Next Gen Stats tracking data, the model forecasts each player’s x and y positions 
across multiple frames, accounting for both offensive and defensive interactions. The goal is to 
minimize the Root Mean Squared Error (RMSE) between predicted and actual trajectories.

---

## Dataset
The dataset is sourced from the **NFL Big Data Bowl 2026** competition and includes:  
- **Tracking data**: Player positions, speed, orientation, and acceleration prior to the ball being thrown.  
- **Targeted receiver info**: Identification of the intended pass recipient.  
- **Ball landing location**: Coordinates where the pass is expected to arrive.  

> Only plays where the ball is in the air for more than 0.5 seconds are considered; quick passes, throwaways, and 
 deflected passes are excluded.

---

## Features
- Player speed, acceleration, and orientation  
- Distance to ball landing location  
- Relative distance to nearest opponents and teammates  
- Directional angles toward ball and other players  
- Multi-agent interaction features for team dynamics  

---

## Modeling Approach
- **Baseline Model**: LSTM to predict sequential x, y positions per player.  
- **Advanced Models**:  
  - Transformer-based sequence-to-sequence modeling  
  - Graph Neural Networks (GNN) to capture interactions between players  
  - Probabilistic forecasting for multi-modal trajectory prediction  

- **Loss Function**: RMSE between predicted and actual positions  
- **Evaluation**: Offline validation on historical plays; leaderboard evaluation on live data  

---