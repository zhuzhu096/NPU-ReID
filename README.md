# NPU-ReID Dataset  
Visible–Infrared Cross-Modality Person Re-Identification Dataset

## 1. Introduction
NPU-ReID is a large-scale dataset designed for **visible–infrared cross-modality person re-identification**. It contains images captured by **8 cameras** with diverse viewpoints and lighting conditions. The dataset includes both **RGB** (visible light) and **infrared** modalities, enabling research on robust ReID under day/night and indoor/outdoor environments.

This dataset was constructed as part of the master thesis research on cross-modality ReID  
(see dataset description in the original thesis, page references in the uploaded PDF).

---

## 2. Key Features
- **Balanced modalities:** nearly equal numbers of RGB and IR images  
- **Rich viewpoint variation:** front, back, side, diagonal views  
- **High-resolution imagery:** captured at 1920×1080  
- **Day & night coverage:** aligned RGB/IR camera pairs  
- **Bounding-box labels included:** suitable for detection & ReID  
- **Two dataset scales available:**  
  - **NPU-ReID-L**: 600 identities  
  - **NPU-ReID-S**: 310 identities  

---

## 3. Dataset Statistics

| Version | IDs | RGB Images | IR Images | Total Images | Cameras |
|--------|-----|------------|-----------|--------------|---------|
| **NPU-ReID-S** | 310 | 16,980 | 19,500 | 36,480 | 8 |
| **NPU-ReID-L** | 600 | 34,621 | 38,578 | 73,199 | 8 |

Image size distribution and pixel-level statistics are analyzed in the thesis (pages 18–23), showing consistent quality across RGB and IR sensors.

---

## 4. Camera Setup
- **4 RGB cameras + 4 IR cameras**  
- Installed across **indoor and outdoor** locations  
- Same model for each modality to ensure consistency  
  - RGB: *DS-2CD3T26WDV3-L*  
  - IR: *DS-IPC-B12V2-1*  
- Resolutions: **1920×1080**  
- Night IR illumination up to **50 meters**

---

## 5. Data Acquisition & Annotation
- Collected continuously for **7 days** using synchronized camera streams  
- Frame extraction at **1 frame per 10 frames** (≈2.5 FPS)  
- Bounding boxes manually annotated using **DarkLabel** with multi-target tracking  
- Each ID contains images with diverse poses and camera viewpoints

---

---

## 6. Train/Test Protocol

### **NPU-ReID-L**
- **Train:** 480 IDs  
- **Test:** 120 IDs  

### **NPU-ReID-S**
- **Train:** 248 IDs  
- **Test:** 62 IDs  

### **Evaluation Modes**
- **RGB → IR** matching  
- **IR → RGB** matching  
- **Indoor-only**, **Outdoor-only**, or **All-search** modes  
- **Single-shot** and **Multi-shot** gallery options

These protocols follow common practices in SYSU-MM01 and RegDB datasets, but with improved modality balance.

---

## 7. Benchmarking
The dataset is compatible with:
- Transformer-based models (e.g., Swin-Transformer, TransReID)
- CNN-based models (ResNet, DenseNet)
- Metric learning frameworks (triplet loss, contrastive loss)
- Multi-modal fusion architectures

Performance baselines from the thesis (e.g., Tri-former framework) can be added here.

---

## 8. Citation
If you use NPU-ReID in your research, please cite the original thesis: 
Dual-Stream Transformer with Cross-Modality Alignment for Person Re-Identification


---

## 9. License
This dataset is intended **for academic research only**.  
Commercial use is not permitted.  
Please check the repository license file for details.

---

## 10. Contact
If you have questions regarding the dataset or usage, please open an issue in this repository.
