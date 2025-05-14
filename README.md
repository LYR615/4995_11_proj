### How to Run

1. Clone the repo and open the notebook:

   ```bash
   git clone https://github.com/LYR615/4995_11_proj/tree/main
   ```

2. Mount Google Drive and adjust the paths:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. Run all cells in `ViT_OE.ipynb`.

    

### Dependencies

- Python 3.8+
- PyTorch
- torchvision
- pandas, numpy, matplotlib
- scikit-learn
- PIL

You can install dependencies using:

```bash
pip install torch torchvision pandas scikit-learn matplotlib pillow
```



### Output

Model weights and test predictions will be saved to:

```
/content/drive/MyDrive/Released_Data_NNDL_2025/test_predictions/
```



### Dataset & Scripts Overview

This repository includes several key folders and scripts for handling novel-class training:

- **`train_images_novel/`**
  Contains manually collected images from novel super-classes and sub-classes. These are used to support novelty-aware classification.

- **`train_images_with_novel/`** 
  Merged dataset that includes both original (seen) images and the newly added novel images. Used as the final training image directory.

- **`data_exploration_preprocessing.ipynb`** 
  Preprocessing notebook that merges the original and novel label CSVs into a single file (`train_data_novel.csv`). It also includes exploratory data analysis on the class distributions.

- **`train_data_novel.csv`** 
  A CSV file containing image filenames and their corresponding super-class and sub-class labels, covering both seen and novel categories.

- **`ViT_OE.ipynb`** 
  Main training script for the OE ViT model. 
  **Important paths used in this notebook:**
  - `train_ann_df` → Points to `train_data_novel.csv` (available in this repo).
  - `train_img_dir` → Should be set to `train_images_with_novel/` (available in this repo).
  - All other paths (e.g., test images, submission CSV) are from the original `Released_Data_NNDL_2025` folder provided for the project.
