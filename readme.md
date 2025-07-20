# 🐞 Ladybug Classification Project

Welcome to my ladybug classification project — developed as part of a machine learning course at **ISEP**.

The goal: 🧠 Automatically **classify ladybugs into two distinct species** using a custom image processing pipeline and interpretable machine learning models.

---

## 🔬 The Two Species

We focused on distinguishing between two species of ladybugs:

- 🐞 **European Ladybug** (*Coccinella septempunctata*): Classic red shell with 7 black spots.
- 🐞 **Asian Ladybug** (*Harmonia axyridis*): More color variation and often more spots or even a full black shell.

One of the biggest challenges was to **design and extract our own features**, rather than using deep learning, so that the classification process remained fully explainable.

---

## 📁 Dataset Overview

- **Training set**: Located in [`/ladybug/`](./ladybug/), it contains:
  - RGB images: e.g., `im001_im.png`
  - Segmented shell images: e.g., `im001_seg.png`

- **Test set**: Found in [`/test/`](./test/), with the same structure. This set was kept unseen during training for final evaluation.

> ✨ Each image is paired with a row in a `.csv` file containing extracted features.

---

## 🧪 Features Extraction

We built a custom pipeline to extract features from both RGB and segmented images.  
These include:

- Color statistics
- Spot detection
- Shell color analysis
- Grayscale thresholds

📓 Full details are available in the [features extraction notebook](./feature_extraction.ipynb).

---

## 🤖 Classification & Results

The [classification notebook](./classification.ipynb) contains the model training and evaluation process.

We tested multiple **interpretable models** and achieved the **best results with a Decision Tree**:

### ✅ Final Accuracy: **94% on test data**

> ✔️ This model allows visual inspection of decisions and offers full transparency into how classification is made.

---

## 🖼️ Sample Image

Here’s an example of a training image used in our dataset:

![RGB Ladybug](https://github.com/godefroylmb/Ladybug/blob/main/ladybug/im-001_im.png?raw=true)

And its corresponding segmentation:

![Segmented Ladybug](https://github.com/godefroylmb/Ladybug/blob/main/ladybug/im-001_seg_viz.png?raw=true)

---

## 📂 Key Files

| File                          | Description |
|------------------------------|-------------|
| `training_labels.md`         | Raw labels for training set |
| `training_labels_completed.csv` | Features + labels for training (post-extraction) |
| `test_labels.md`             | Raw labels for test set (only used for evaluation) |
| `test_labels_completed.csv`  | Features + labels for test set (post-extraction) |
| `predicted_labels.csv`       | Model predictions on test set |
| `feature_extraction.ipynb`   | Notebook used to extract features |
| `classification.ipynb`       | Notebook for training and testing models |

---

## 🧠 Why This Approach?

Rather than relying on opaque models like deep learning, we opted for interpretable, feature-driven classification so that we could:

- Control the logic of the system
- Understand how each decision is made
- Debug, tune, and improve with confidence

---

## 📬 Questions?

If you’re curious about our feature engineering or want to try other models, feel free to explore the notebooks or reach out!

