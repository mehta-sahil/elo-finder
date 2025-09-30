# Chess Elo Rating Prediction

## Project Goal
To predict the Elo ratings for White and Black players based on game move analysis from the Stockfish engine.

---

## Dataset
This project uses the ["Finding Elo" dataset from Kaggle](https://www.kaggle.com/competitions/finding-elo/data). The key files are:
* `data_uci.pgn`: Contains game data, including the true Elo ratings used for training.
* `stockfish.csv`: Contains the centipawn evaluation scores for each move in the games.
* `sampleSubmission.csv`: Shows the required output format.

---

## Live Performance Prediction
Beyond the initial model training, this project includes an interface for analyzing a new game. After two players complete a match, the system can:
1.  **Record the Game:** The moves from the new game are saved.
2.  **Analyze with Stockfish:** Each move is processed by the Stockfish engine to generate a sequence of centipawn scores, just like the training data.
3.  **Calculate Performance:** The same features (average centipawn loss, etc.) are calculated from the new move scores.
4.  **Predict Elo:** The pre-trained models are used to predict a performance Elo for both the White and Black players based on the quality of their moves in that single game.

---

## Requirements
The script requires the following Python libraries:
* `pandas`
* `numpy`
* `scikit-learn`
* `lightgbm`
* `python-chess`

Install them using pip:
```bash
pip install pandas numpy scikit-learn lightgbm python-chess
