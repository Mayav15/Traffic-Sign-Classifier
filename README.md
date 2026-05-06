# Traffic Sign Classifier

A deep-learning traffic sign classifier built with **Keras / TensorFlow** that recognizes 43 classes of German road signs from arbitrary uploaded images. Includes a Tkinter GUI so non-developers can use it.

## Highlights

- **Dataset:** [German Traffic Sign Recognition Benchmark (GTSRB)](https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign) — ~50,000 images across 43 classes
- **Model:** Convolutional Neural Network (CNN) trained in Keras
- **Artifact:** trained model serialized as [`Traffic_Classifier.h5`](./Traffic_Classifier.h5), ready to load for inference
- **GUI:** Tkinter app for upload-and-classify in one click

## Architecture

```
Image upload (Tkinter)
       │
       ▼
[ Preprocessing — resize, normalize ]
       │
       ▼
[ CNN forward pass — Keras ]
       │
       ▼
Top class + confidence
       │
       ▼
[ Tkinter result panel ]
```

## Files

| File | Purpose |
|------|---------|
| [`Traffic-Sign-Classifier-Model.ipynb`](./Traffic-Sign-Classifier-Model.ipynb) | Training notebook: data loading, augmentation, CNN architecture, training loop, evaluation |
| [`Traffic-Sign-Classifier-GUI.ipynb`](./Traffic-Sign-Classifier-GUI.ipynb) | Tkinter inference GUI |
| [`Traffic_Classifier.h5`](./Traffic_Classifier.h5) | Saved Keras model weights |

## Tech Stack

- Python 3.x
- TensorFlow / Keras (CNN)
- OpenCV / PIL (image preprocessing)
- Tkinter (GUI)
- NumPy, Matplotlib (training notebook)

## Running

### Train (optional — model already included)
Open `Traffic-Sign-Classifier-Model.ipynb` in Jupyter and run all cells. Requires the GTSRB dataset.

### Inference GUI
```bash
pip install tensorflow opencv-python pillow numpy matplotlib
jupyter notebook Traffic-Sign-Classifier-GUI.ipynb
```

Then run the notebook — a Tkinter window opens. Click **Upload Image**, pick a sign, and read the prediction.

## Dataset

- Source: https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign
- 43 classes, ~50K images
- Standard split: 39,209 train / 12,630 test
