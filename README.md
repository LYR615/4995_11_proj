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

