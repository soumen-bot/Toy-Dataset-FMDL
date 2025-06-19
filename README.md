# Tic-Tac-Toe Rotated Dataset ⭕❌

This repository contains code to generate a synthetic image classification dataset based on the classic game of **Tic-Tac-Toe**. The dataset is designed to evaluate AGEConv model.
To get obtain the tic tac toe images run the cells of the jupyter notebook and images would be saved in a folder named ttt_dataset_clean_rotated with a label.csv containing the image_name and its corresoponding labels. 
## Dataset Description

Each image represents a valid state of a 3×3 Tic-Tac-Toe board. The classification task is to predict the **winner**:

- `Class 0`: X wins  
- `Class 1`: O wins  
- `Class 2`: No winner (draw or in-progress)

Each board is augmented by applying **rotations (0°, 90°, 180°, 270°)** to test whether models can detect win conditions **regardless of spatial orientation**.

## 📂 Output Structure

After running the dataset generation script, the following structure is created:

ttt_dataset/
-├── 00001_rot0.png
-├── 00002_rot90.png
-├── ...
-├── labels.csv # Contains filenames and corresponding labels

- Images are grayscale (`.png`) and of shape `96×96` pixels (configurable).
- The CSV file contains two columns:
  - `filename`: name of the image file
  - `label`: 0 (X wins), 1 (O wins), or 2 (no winner)

