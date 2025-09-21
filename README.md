# SABMIS: Sparse Approximation Based Blind Multi-Image Steganography Scheme

This repository contains MATLAB code and sample images for the paper:  
**SABMIS: Sparse Approximation Based Blind Multi-Image Steganography Scheme**  
Rohit Agrawal, Kapil Ahuja, Marc C. Steinbach, Thomas Wick  
Published in *PeerJ Computer Science, 2022*  

---

## Abbreviations
- **PSNR**: Peak Signal-to-Noise Ratio  
- **SSIM**: Mean Structural Similarity Index  
- **NCC**: Normalized Cross-Correlation Coefficient  
- **NAE**: Normalized Absolute Error  

---

## Data Files (Images)

1. `Fruits.png`  
2. `peppers_gray.tif`  
3. `Boat.png`  
4. `House.tif`  
5. `Lake.tif`  
6. `Stream.tif`  *(called “Stream” in the manuscript)*  
7. `Livingroom.tif`  
8. `Tulips.png`  
9. `jetplane.tif`  
10. `Cameraman.tif`  
11. `BrainImage.bmp`  
12. `Mammogram1.png`  
13. `Mammogram2.png`  
14. `Mammogram3.png`  
15. `Mammogram4.png`  

---

## Code Files (MATLAB)

1. `MultiImageSteg.m` – Main code file for embedding  
2. `ImageSampling.m` – Performs image sampling  
3. `lasso_my.m` – Stego-image construction (ADMM solution of LASSO)  
4. `ssim.m` – Computes mean SSIM  
5. `NAE.m` – Computes NAE values  
6. `ImageInverseSampling.m` – Performs inverse image sampling  
7. `PSNR_Graphs.m` – Generates PSNR plots  

**Additional variants:**
- `MultiImageSteg_RestrictOversampling.m`  
  Main code with restricted oversampling (Appendix D).  
- `MultiImageSteg_Hide6Images.m`  
  Main code when hiding six images (Appendix E).  

---

## Parameters (from manuscript)

```matlab
b      = blk_Cover       = 8        % block size
b^2    = BlkSize_Cover   = 64
p1     = cof_Cover       = 32
p2     = n_col           = b^2 - p1 = 32
m      = n_row           = 10 * n_col
p3     = cof_Secret      = 32
l      = blk_Secret      = 8
alpha  = 0.01
beta   = 0.1
gama   = 1
temp1  = c = 6
---

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
