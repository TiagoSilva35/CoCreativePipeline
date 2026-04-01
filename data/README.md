# Data Directory Structure

This project uses the MovieLens 100K dataset.

Data root location in this repository:

- ./data/

Current structure:

- ml-100k/: extracted MovieLens 100K files
  - includes core files such as u.data, u.item, u.user, u.genre, and predefined train/test splits (u1.base, u1.test, ..., ub.base, ub.test)

Notes:

- The notebook should read data from ./data/ml-100k/
- There is no separate data root directory required outside ./data/

Source:
- https://files.grouplens.org/datasets/movielens/ml-100k.zip
