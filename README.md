# Spectro-polarimetric Dataset

We provide a spectro-polarimetric dataset. This dataset consists of full-Stokes images for both hyperspectral and trichromatic scenes. Hyperspectral dataset has 311 scenes and trichromatic dataset has 2022 scenes.

For more details, see our paper on [<u>**Spectral and Polarization Vision: Spectro-polarimetric Real-world Dataset**</u>](https://arxiv.org/abs/2311.17396).

## 📦 Contents
- [**File Hierarchy** ](#💾-file-hierarchy)
- [**Trichromatic Data Overview** ](#📷-trichromatic-data-overview)
- [**Hyperspectral Data Overview** ](#📷-hyperspectral-data-overview)
- [**Labeling Information** ](#🗂️-labeling-information)
- [**Citation** ](#📜-citation)
- [**Contact** ](#📫-contact)

## 💾 File Hierarchy
- ### **📂 trichromatic/**: Trichromatic polarimetric dataset
  - **📂 original/**: Data processed from captured raw files
     - **📄 0000.npy ~**
  - **📂 denoised/**: Data processed from denoised raw files
    - **📄 0000.npy ~**
  - **📂 mask/**: Masks for the scenes
    - **📄 0000.png ~**
  - **📄 labeling_trichromatic.csv**: Labeling each scene
- ### **📂 hyperspectral/**: Hyperspectral polarimetric dataset
  - **📂 original/**: Data processed from captured raw files
    - **📄 0000.npy ~**
  - **📂 denoised/**: Data processed from denoised raw files
    - **📄 0000.npy ~**
  - **📂 mask/**: Mask fors the scenes
    - **📄 0000.png ~**
  - **📄 labeling_hyperspectral.csv**: Labeling each scene
- ### **📄 README.md**


## 📷 Trichromatic Data Overview

+ **original & denoised:**
  - Format: Stokes numpy files `(1900, 2100, 4, 3)`
  - Dimensions:
    - **R:** Spatial dimension
    - **C:** Spatial dimension
    - **s:** Stokes axis (*s0, s1, s2, s3*)
    - **c:** Spectral axis (R G B)

+ **mask:**
  - Binary mask images `(1900, 2100)`
  - Dimensions:
    - **R:** Spatial dimension
    - **C:** Spatial dimension
<!--   
+ **original & denoised**: Stokes numpy files (`(1900, 2100, 4, 3)` format) with dimensions:
  - **R**: Spatial dimension
  - **C**: Spatial dimension
  - **s**: Stokes axis (*s0, s1, s2, s3*)
  - **c**: Spectral axis (RGB for trichromatic dataset)
+ **mask**: Binary mask images (0 or 255) (`(1900, 2100)` format) with dimensions:
  - **R**: Spatial dimension
  - **C**: Spatial dimension -->


## 📷 Hyperspectral Data Overview

+ **original & denoised:**
  - Format: Stokes numpy files `(512, 612, 4, 21)`
  - Dimensions:
    - **R:** Spatial dimension
    - **C:** Spatial dimension
    - **s:** Stokes axis (*s0, s1, s2, s3*)
    - **c:** Spectral axis (`450nm ~ 650nm` at `10nm` intervals)

+ **mask:**
  - Binary mask images `(512, 612)`
  - Dimensions:
    - **R:** Spatial dimension
    - **C:** Spatial dimension


## 🗂️ Labeling Information
- **SceneNum:** Indices of scenes (`0 ~ 310` for hyperspectral, `0 ~ 2021` for trichromatic)
- **Content:** Type of content (scene, object)
- **Timezone:** Scene environment (indoor, day, night)
- **Illumination:** Illumination condition (white, yellow, sunny, cloudy)

## 📜 Citation
```bibtex
@inproceedings{jeon2024spectral,
  title={Spectral and Polarization Vision: Spectro-polarimetric Real-world Dataset},
  author={Jeon, Yujin and Choi, Eunsue and Kim, Youngchan and Moon, Yunseong and Omer, Khalid and Heide, Felix and Baek, Seung-hwan},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  year={2024}
}
```

## 📫 Contact
If you have any questions, please contact
+ Yujin Jeon: jyj7913@postech.ac.kr
+ Eunsue Choi: ches7283@postech.ac.kr
+ Seung-hwan Baek: shwbaek@postech.ac.kr


