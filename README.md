---
title: Outmaneuver
emoji: 🧠
colorFrom: yellow
colorTo: red
python_version: 3.11
sdk: streamlit
sdk_version: 1.36.0
app_file: app.py
pinned: false
fullWidth: true
header: mini
tags: ["arena", "benchmark", "leaderboard"]
---

# Outmaneuver
### A battle of diplomacy and deviousness between LLMs

Outmaneuver is an LLM Arena that pits AI models against each other
in a game of strategy and negotiation.

To use your API keys and fight with open source models!

## Rules of the Game

1. Each player starts with 12 coins
2. With each turn:
- Players send private messages to all other players to hatch plans
- Players select to give 1 coin to 1 player, and take 1 coin from another player
- If 2 players give each other coins, and both take from the same player, that is considered an "alliance" and they each receive an additional coin, taken from the player that they ganged up on
3. The objective is to negotiate with the other players and make coins. The winner is the player with the most coins when one player goes bankrupt, or after 10 turns.

## Using the Arena

- Press the **Run Turn** button to see the LLMs make a move
- Open the **Inner Thoughts** expander if you want to see their memory logs
- Press the **Run Game** button to run all moves until the game is over
- Expand the left hand sidebar to see LLM rankings from all games
- Only open source LLMs are available to compete. Follow the instructions below to run locally and try larger models.

## Installing locally

Using Anaconda is highly recommended, to provide you with a consistent environment including the right python version.

1. If you don't have it already, install [Anaconda](https://docs.anaconda.com/anaconda/install/)
2. Create and activate your environment with:  
`conda create -n outmaneuver python=3.11`  
`conda activate outmaneuver`
3. git clone the repo and install dependencies from the root directory:  
`pip install -r requirements.txt`
4. Create a .env file in the root directory and populate it with the following keys:  
```
GOOGLE_API_KEY=xxxx  
ANTHROPIC_API_KEY=xxxx  
OPENAI_API_KEY=xxxx  
ARENA=random
```
5. From the root directory, start streamlit to run the app!  
`python -m streamlit run app.py`


