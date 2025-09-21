# SABMIS: Sparse Approximation Based Blind Multi-Image Steganography Scheme

## Abbreviations
..............
PSNR (Peak Signal-to-Noise Ratio) 
SSIM (mean Structural Similarity) index 
NCC (Normalized Cross-Correlation) coefficient
NAE (Normalized Absolute Error)

---------------------------------------------------------

## Name Data Files (Images)
......................
1. Fruits.png
2. peppers_gray.tif
3. Boat.png
4. House.tif
5. Lake.tif
6. Stream.tif              (Stream name in the manuscript)
7. Livingroom.tif
8. Tulips.png
9. jetplane.tif
10. Cameraman.tif 
11. BrainImage.bmp
12. Mammogram1.png
13. Mammogram2.png
14. Mammogram3.png
15. Mammogram4.png
--------------------------------------------------------

## Code Files (Matlab) 
..................
1. MultiImageSteg.m - Main code file for embedding
2. ImageSampling.m - file used to perform sampling of image
3. lasso_my.m - file used for the stego-image construction (i.e. ADMM solution of LASSO)
4. ssim.m - file is used to find mean SSIM
5. NAE.m - file is used to find NAE values
6. ImageInverseSampling.m - file to perform image inverse sampling
7. PSNR_Graphs.m file to obtain figure of PSNR values

8. MultiImageSteg_RestrictOversampling.m - Main code file for embedding when we restrict oversampling (discussed in Appendix D "Sensitivity Of our Scheme with Respect to the Novel Components")
9. MultiImageSteg_Hide6Images.m - Main code file for embedding when we hide six images (discussed in Appendix E "A Possible Scenario where our Scheme is not The best")

--------------------------------------------------------

## Parameters Coded in files (same as in the manuscript)
.....................................................
b = blk_Cover = 8 (block size)
b^2 = BlkSize_Cover = 8 * 8 = 64
p1 = cof_Cover = 32
p2 = n_col = b^2 - p1 = 32
m = n_row = 10 * n_col   
p3 = cof_Secret = 32     
l = blk_Secret = 8;
alpha = 0.01
beta = 0.1
gama = 1
temp1 = c = 6

--------------------------------------------------------

## How to Run
..........
1) Images and Matlab files must be in the same folder
2) >> MultiImageSteg
3) >> MultiImageSteg_RestrictOversampling              (for code when we restrict oversampling)
4) >> MultiImageSteg_Hide6Images							(for code when we hide six images)
--------------------------------------------------------

## Third Party Code
................

a) For the ADMM (Alternating Direction Method of Multipliers) solution of the LASSO (Least Absolute Shrinkage and Selection Operator) formulation of the optimization problem, we cited the below paper in our manuscript, and used the Matlab code (lasso_my.m file) provided by the authors (code source web link is also given below).

Paper:- Boyd, S., Parikh, N., Chu, E., Peleato, B., and Eckstein, J. (2010). Distributed optimization and statistical learning via the alternating direction method of multipliers. Foundations and Trends in Machine Learning, 3(1):1–122.

Matlab Code Source:- https://web.stanford.edu/~boyd/papers/admm/lasso/lasso.html (Accessed on 26th october 2021)

b) For mean SSIM (Structural Similarity Index Measure), we cited the below paper in our manuscript, and used the Matlab code (ssim.m file) provided by authors (code source web link is also given below).

Paper:- Wang, Z., Bovik, A., Sheikh, H., and Simoncelli, P. (2004). Image quality assessment: From error visibility to structural similarity. IEEE Transactions on Image Processing, 13(4):600–613.

Matlab Code Source:- http://www.ece.uwaterloo.ca/~z70wang/research/ssim/ (Accessed on 26th october 2021)

--------------------------------------------------------
## Citation

If you use this code in your research, please cite: # Insert/Update the citation once arxiv is available

```
@article{singh2025chameleon2++,
  title={Chameleon2++: An efficient chameleon2 clustering with approximate nearest neighbors},
  author={Singh, Priyanshu and Ahuja, Kapil},
  journal={arXiv preprint arXiv:2501.02612},
  year={2025}
}
```
