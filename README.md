# cnn-selfie-recognition

This project explores whether a Convolutional Neural Network (CNN), trained solely on selfies, can generalize to real-world, non-selfie images for the task of person recognition. It was built using a VGG16 base model with pre-trained ImageNet weights and a custom classifier layer.

---

## 🧠 Objective

Investigate the generalization power of selfie-trained CNNs:
- Can a model trained on easily gathered selfie data identify people in everyday photos?
- How does data quality and augmentation impact real-world performance?

---

## 📁 Project Contents

- `cnn_person_recognition.ipynb`  
  → Main Google Colab notebook with model architecture, training process, evaluation, and experiments.

- `cnn_selfie_recognition_essay.pdf`  
  → Full write-up detailing all iterations, insights, and conclusions.

- `cnn_selfie_recognition_slidedeck.pdf`  
  → Slide deck summarizing project scope, experiments, and final results.

---

## 📊 Key Results

<table>
  <tr>
    <th>Experiment</th>
    <th>Selfie Accuracy</th>
    <th>Real-World Accuracy</th>
  </tr>
  <tr>
    <td>Base VGG16 + Custom Head</td>
    <td>100%</td>
    <td>50%</td>
  </tr>
  <tr>
    <td>Balanced Classes + Augmentation</td>
    <td>85%</td>
    <td>40%</td>
  </tr>
  <tr>
    <td>Unfrozen Top 10 Layers</td>
    <td>28%</td>
    <td>-</td>
  </tr>
  <tr>
    <td>CV2 Face Cropping</td>
    <td>94%</td>
    <td>30%</td>
  </tr>
</table>

---

## 🔬 Key Takeaways

- **Data tuning > model tuning** for small, user-generated datasets.
- **Selfie-trained CNNs** can moderately generalize to real-world images with class balance and cleanup.
- Overfitting to ImageNet weights or over-augmentation can hurt performance.

---

## 🔮 Future Work

- Try other model architectures like ResNet or EfficientNet.
- Expand dataset with more individuals and real-world contexts.
- Test few-shot learning or contrastive approaches (e.g., Siamese Networks).

---
