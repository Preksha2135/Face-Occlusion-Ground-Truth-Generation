# Face Occlusion Ground Truth Generation

This project implements **Face Occlusion Detection** using DeepLabV3+ to generate **ground truth images** for occluded face images. The output consists of binary masks with two classes:

- **Black (0)** - Background
- **White (255)** - Occlusion

The dataset used is **WebFace OCC**, but the full dataset is available only upon request from [**huangbaojin@whu.edu.cn**](mailto\:huangbaojin@whu.edu.cn).

## Features

- Uses **DeepLabV3+ with ResNet-101** backbone for segmentation.
- Generates **ground truth occlusion masks** for face images.
- Processes **nested folder structures** for batch mask generation.
- Outputs **grayscale binary masks** (background vs occlusion).

## Dataset

The project is trained using **WebFace OCC**. However, due to restrictions, the complete dataset is **not included**. If you require the full dataset, you must request access from:

📧 [**huangbaojin@whu.edu.cn**](mailto\:huangbaojin@whu.edu.cn)

## Installation

To run this project, install the required dependencies:

```bash
pip install torch torchvision numpy pillow matplotlib
```

## Usage

### 1. Training the Model

Modify dataset paths in `face_occlusion_ground_truth_generation.py` and run:

```bash
python face_occlusion_ground_truth_generation.py
```

### 2. Generating Ground Truth Masks for New Images

Note that initially 14 ground truth images are created manually using Adobe Photoshop in order to train the model. I've given access to the same in the assets/GroundTruth. 
To generate masks for a folder of images, update `train_image_dir`, `train_mask_dir`, `input_folder` and `output_folder` in the script and run:

```bash
python face_occlusion_ground_truth_generation.py
```

## Model

The project uses **DeepLabV3+ with a ResNet-101 backbone**, pre-trained on COCO, and fine-tuned for **occlusion segmentation** with **two classes**:

1. **Occlusion (White - 255)**
2. **Background (Black - 0)**

## Example Output

![alt text](https://github.com/Preksha2135/Face-Occlusion-Ground-Truth-Generation/blob/main/output.jpg?raw=true)

## Contributions

Feel free to contribute by improving the segmentation model or optimizing the dataset usage. Submit a pull request if you'd like to collaborate!

## License

This project is for **research purposes only**. Please cite the dataset owners if you use WebFace OCC.

---

### Contact

For any queries, feel free to reach out!

