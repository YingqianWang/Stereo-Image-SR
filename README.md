### <img src="https://raw.github.com/YingqianWang/Awesome-Stereo-Image-SR/master/Fig/Thumbnail.jpg" width="1000">
#### With recent advances in stereo vision, dual cameras are commonly adopted in mobile phones and autonomous vehicles. Using the complementary information provided by binocular systems, the resolution of image pairs can be enhanced by stereo image super-resolution (SR) algorithms. In this repository, we present a collection of papers and datasets on stereo image SR, together with their codes and repos. 
#### Note: This repository will be updated on a regular basis, so stay tuned~~🎉🎉🎉

## Datasets

|     Name     |   links |  Comments |
| :----------: |  :-----: | :-------: |
|     **Flickr1024**     | [**website**](https://yingqianwang.github.io/Flickr1024/) & [**paper**](http://openaccess.thecvf.com/content_ICCVW_2019/papers/LCI/Wang_Flickr1024_A_Large-Scale_Dataset_for_Stereo_Image_Super-Resolution_ICCVW_2019_paper.pdf) | **large-scale; high-quality images; diverse senarios** |
|     **Middlebury**     | [**website**](http://vision.middlebury.edu/stereo/data/) & [**paper**](https://elib.dlr.de/90624/1/ScharsteinEtal2014.pdf) | **indoor scenarios; groundtruth disparity** |
|     **KITTI2012**     | [**website**](http://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo) & [**paper**](http://ww.cvlibs.net/publications/Geiger2012CVPR.pdf) | **driving perspectives; groundtruth disparity** |
|     **KITTI2015**     | [**website**](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) & [**paper**](http://openaccess.thecvf.com/content_cvpr_2015/papers/Menze_Object_Scene_Flow_2015_CVPR_paper.pdf) | **driving perspectives; groundtruth disparity** |


## Methods
|     Aronym & Codes    |  Paper  | Demonstrated Superior to |
| :----------: |  :----------------------------------------------------------------: | :----------: |
| [**StereoSR**](https://github.com/PeterZhouSZ/stereosr) | [**Enhancing the Spatial Resolution of Stereo Images using a Parallax Prior**](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf), ***CVPR2018***. | *SRCNN, VDSR*
| [**PASSRnet**](https://github.com/LongguangWang/PASSRnet) | [**Learning Parallax Attention for Stereo Image Super-Resolution**](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf), ***CVPR2019 & TPAMI2020***. | **StereoSR**,<br> *SRCNN, VDSR, DRCN, DRRN, LapSRN*
| [**SAM**](https://github.com/XinyiYing/SAM) | [**A Stereo Attention Module for Stereo Image Super-Resolution**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204), ***SPL2020.*** | *SRResNet* < **PASSRnet** < *SRResNet+SAM* |
| **SPAMnet** | **Stereoscopic image super-resolution with stereo consistent feature**, ***AAAI2020.*** | **StereoSR, PASSRnet**,<br> *SRCNN, VDSR, DRRN, LapSRN* |
| **DASSR** | [**Disparity-Aware Domain Adaptation in Stereo Image Restoration**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yan_Disparity-Aware_Domain_Adaptation_in_Stereo_Image_Restoration_CVPR_2020_paper.pdf), ***CVPR2020.*** | **StereoSR, PASSRnet**,<br> *EDSR, SRNTT, DUF, SMPC* |
| **IMSSRnet** | **Deep Stereoscopic Image Super-Resolution via Interaction Module**, ***TCSVT2020.*** | **StereoSR, PASSRnet** |
| [**CPASSRnet**](https://github.com/canqChen/CPASSRnet) | **Cross Parallax Attention Network for Stereo Image Super-Resolution**, ***TMM2021.*** | **StereoSR, PASSRnet**, <br> *SRCNN, LapSRN，SRDense* |
| [**BSSRnet**](https://github.com/xuqingyu26/BSSRnet) | [**Deep Bilateral Learning for Stereo Image Super-Resolution**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9382858), ***SPL2021.*** | **StereoSR, PASSRnet, SRRes+SAM**, <br> *VDSR, LapSRN，DRRN* |
| [**iPASSR**](https://github.com/YingqianWang/iPASSR) | [**Symmetric Parallax Attention for Stereo Image Super-Resolution**](https://arxiv.org/pdf/2011.03802.pdf), ***CVPRW2021.*** | **StereoSR, PASSRnet, SRRes+SAM**,<br> *EDSR, RDN, RCAN* |

## Benchmark
|     Method     |  Scale  | #Params. |  KITTI 2012  |  KITTI 2015  |  Middlebury  |  Flickr1024  |
|:--------------:|  :----: | :------: | :----------: | :----------: | :----------: | :----------: |
|     Bicubic	   |    2×	 |    —     | 28.51/0.8842 | 28.61/0.8973	| 30.60/0.8990 | 24.94/0.8186 |
|     VDSR  	   |    2×	 |   0.66M  | 30.30/0.9089 | 29.78/0.9150	| 32.77/0.9102 | 25.60/0.8534 |
|     EDSR  	   |    2×	 |   38.6M  | 30.96/0.9228 | 30.73/0.9335	| 34.95/0.9492 | 28.66/0.9087 |	
|     RDN   	   |    2×	 |   22.0M  | 30.94/0.9227 | 30.70/0.9330	| 34.94/0.9491 | 28.64/0.9084 |					
|     RCAN   	   |    2×	 |   15.3M  | 31.02/0.9232 | 30.77/0.9336	| 34.90/0.9486 | 28.63/0.9082 |				
|     StereoSR   |    2×	 |   1.08M  | 29.51/0.9073 | 29.33/0.9168	| 33.23/0.9348 | 25.96/0.8599 |		 			
|     PASSRnet   |    2×	 |   1.37M  | 30.81/0.9190 | 30.60/0.9300	| 34.23/0.9422 | 28.38/0.9038 |		 			
|     iPASSR     |    2×	 |   1.37M  | 31.11/0.9240 | 30.81/0.9340	| 34.51/0.9454 | 28.60/0.9097 |			
			



<!--
| **DCSSRnet** | **--ICLRW2020--**<br> [**paper**](https://arxiv.org/pdf/2003.08539.pdf) | -- | **endoscopic image, disparity-constrained parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN* |
| **NNRANet** | **--ICASSP2020--**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9054687) | -- | **non-local, nested residual group** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |
-->
