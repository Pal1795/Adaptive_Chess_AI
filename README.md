# ♟️ Adaptive Chess AI

An interactive, real-time chess bot that dynamically adapts to the player's ELO rating and inferred play style. Built using Stockfish, Google Vertex AI (Gemini), and Streamlit.

## Overview

Traditional chess engines play at fixed strengths — either too strong for beginners or too weak for advanced players. This project solves that with an **adaptive chess bot** that:

- Adjusts **difficulty** based on user ELO using Stockfish’s `UCI_Elo` parameter
- Adapts **playing style** (Aggressive, Defensive, Tactical, etc.) based on opponent move patterns
- Uses **LLMs (Gemini 2.0 Flash)** to generate natural, ELO-appropriate moves with human-style explanations
- Offers **real-time feedback** on user moves for educational guidance
- 
## Features

- **ELO-Aware Play**: The bot plays differently at 800 vs. 1800 rating
- **Style Classifier**: Detects opponent behavior and adjusts AI style accordingly
- **LLM-Powered Move Analysis**: Explains why your move was good, bad, or risky
- **Streamlit Interface**: Play directly in a browser, with a real-time SVG board and full controls

---

## Tech Stack

- `python-chess` – board and move logic
- `stockfish` – position evaluation and top-move generation
- `vertexai` – Gemini 2.0 Flash model via Google Cloud
- `Streamlit` – interactive web UI
- `cairosvg + PIL` – SVG-to-image board rendering
