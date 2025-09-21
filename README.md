
# SABMIS: Sparse Approximation Based Blind Multi-Image Steganography Scheme

## Abbreviations

- PSNR (Peak Signal-to-Noise Ratio)
- SSIM (mean Structural Similarity index)
- NCC (Normalized Cross-Correlation coefficient)
- NAE (Normalized Absolute Error)

***

## Name Data Files (Images)

- Fruits.png
- peppers_gray.tif
- Boat.png
- House.tif
- Lake.tif
- Stream.tif (Stream name in the manuscript)
- Livingroom.tif
- Tulips.png
- jetplane.tif
- Cameraman.tif
- BrainImage.bmp
- Mammogram1.png
- Mammogram2.png
- Mammogram3.png
- Mammogram4.png

***

## Code Files (MATLAB)

- MultiImageSteg.m – Main code file for embedding
- ImageSampling.m – Used to perform sampling of image
- lasso_my.m – Used for the stego-image construction (ADMM solution of LASSO)
- ssim.m – Used to find mean SSIM
- NAE.m – Used to find NAE values
- ImageInverseSampling.m – Used to perform image inverse sampling
- PSNR_Graphs.m – Obtain figure of PSNR values
- MultiImageSteg_RestrictOversampling.m – Embedding with restricted oversampling (see Appendix D)
- MultiImageSteg_Hide6Images.m – Embedding when hiding six images (see Appendix E)

***

## Parameters Coded in Files

- b = blk_Cover = 8 (block size)
- b² = BlkSize_Cover = 8×8 = 64
- p1 = cof_Cover = 32
- p2 = n_col = b² – p1 = 32
- m = n_row = 10 × n_col
- p3 = cof_Secret = 32
- l = blk_Secret = 8
- alpha = 0.01
- beta = 0.1
- gama = 1
- temp1 = c = 6

***

## How to Run

1. Place all images and Matlab files in the same folder
2. Run in MATLAB:
    - `>> MultiImageSteg`
    - `>> MultiImageSteg_RestrictOversampling` (restricted oversampling)
    - `>> MultiImageSteg_Hide6Images` (for hiding six images)

***

## Third Party Code

- **ADMM for LASSO:**
Boyd, S., Parikh, N., Chu, E., Peleato, B., and Eckstein, J. (2010). Distributed optimization and statistical learning via the alternating direction method of multipliers. *Foundations and Trends in Machine Learning*, 3(1):1–122.
Code used: lasso_my.m
[Provided by authors](https://web.stanford.edu/~boyd/papers/admm/lasso/lasso.html) (accessed 26 Oct 2021)
- **Mean SSIM:**
Wang, Z., Bovik, A., Sheikh, H., and Simoncelli, P. (2004). Image quality assessment: From error visibility to structural similarity. *IEEE Transactions on Image Processing*, 13(4):600–613.
Code used: ssim.m
[Provided by authors](http://www.ece.uwaterloo.ca/~z70wang/research/ssim/) (accessed 26 Oct 2021)

***

## Citation

If you use this code in your research, please cite:

```
@article{agrawal2022sabmis,
  title={SABMIS: sparse approximation based blind multi-image steganography scheme},
  author={Agrawal, Rohit and Ahuja, Kapil and Steinbach, Marc C and Wick, Thomas},
  journal={PeerJ Computer Science},
  volume={8},
  pages={e1080},
  year={2022},
  publisher={PeerJ Inc.}
}
```

