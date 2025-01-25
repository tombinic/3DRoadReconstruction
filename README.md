# Visual Analysis of Moving Vehicles
🧑‍🤝‍🧑Thanks to [Andrea Bertogalli](https://github.com/andberto) and [Niccolò Balestrieri](https://github.com/NiccoloBalestrieri)
## Project Description

This project focuses on the visual analysis of moving vehicles, specifically on model-based car localization and road reconstruction using a single calibrated static camera. The objectives include identifying the visible wheels of a moving car, extracting the rims due to their higher contrast, and using this information to follow the road profile and collect 3D points on the road surface for interpolation.

## Methodology

### Motivation

The project aims to reduce the cost and complexity of vehicle localization systems by using a single static camera and enhancing accuracy through deep learning techniques. The collected 3D data is valuable for infrastructure maintenance and urban planning.

### Proposed Solution

The pipeline consists of three stages:

1. A Region Proposal Network (RPN) for wheel detection.
2. An ellipse detection algorithm to identify the visible wheels within the proposed regions.

3. Estimation of the 3D point cloud and subsequent surface interpolation.

### State of the Art

The literature addresses this problem with deep learning and classical computer vision techniques, including stereo vision and structure from motion (SfM).

### Camera and Calibration

An iPhone 14 Pro Max camera was used for video acquisition and calibrated using the Zhang method.

### Data Collection

Videos of cars on various roads were recorded to collect data, ensuring that the rims would not be parallel to the image plane or filmed from above.

### Network Architectures

Two deep learning models were used for object detection: a pre-trained ResNet50 model and a YOLOv5-based wheel detector.

### Wheels Detection

An algorithm was designed to select the most probable ellipse representing the wheels' shape and to extract the contact points.

### 3D Reconstruction

Two approaches were proposed for 3D reconstruction: a deep learning-based approach using a monocular depth estimation model (DPT) and a geometric approach using the Perspective-n-Point (PnP) algorithm.

## Results

The results show that the deep learning approach outperforms the geometric approach in 3D reconstruction, with a mean re-projection error of 0.1 pixels.

## Conclusion

The project achieved satisfactory results, with potential for further exploration in the geometric approach and consideration of other vehicle features.

## References


- He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. In Proceedings of the IEEE conference on computer vision and pattern recognition, pages 770–778.
- Rashidi Fathabadi, F., Grantner, J. L., Shebrain, S. A., & Abdel-Qader, I. (2022). Box-trainer assessment system with real-time multi-class detection and tracking of laparoscopic instruments, using CNN. Acta Polytechnica Hungarica, 19(2).

- Shenoda, M. (2023). Lighting and rotation invariant real-time vehicle wheel detector based on YOLOv5. arXiv preprint arXiv:2305.17785.
- Fitzgibbon, A. W., Pilu, M., & Fisher, R. B. (1999). Direct least-squares fitting of ellipses. 21(5):476–480.

- Ranftl, R., Bochkovskiy, A., & Koltun, V. (2021). Vision transformers for dense prediction. In Proceedings of the IEEE/CVF international conference on computer vision, pages 12179–12188.
- Dosovitskiy, A., Beyer, L., Kolesnikov, A., Weissenborn, D., Zhai, X., Unterthiner, T., ... & Houlsby, N. (2020). An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929.

- Lepetit, V., Moreno-Noguer, F., & Fua, P. (2009). EPnP: An accurate O(n) solution to the PnP problem. International Journal of Computer Vision, 81(2), 155–166.
- Zheng, Y., Kuang, Y., Sugimoto, S., Aström, K., & Okutomi, M. (2013). Revisiting the PnP problem: A fast, general and optimal solution. In 2013 IEEE International Conference on Computer Vision, pages 2344–2351.


---

This README file provides an overview of the "Visual Analysis of Moving Vehicles" project conducted in the Image Analysis and Computer Vision course, A.Y. 2023-2024, under the supervision of Prof. Vincenzo Caglioti. The project was carried out by Niccolò Balestrieri, Andrea Bertogalli, and Nicolò Tombini from Politecnico di Milano, Italy.

For more detailed information, please refer to the project documentation and source code provided in this repository.
