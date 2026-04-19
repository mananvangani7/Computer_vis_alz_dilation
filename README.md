# Alzheimer's Disease Classification — CNN with Dilated Convolutions

Six-stage Alzheimer's disease classification using the ADNI MRI dataset. The core contribution is a custom CNN architecture incorporating dilated convolutions for enhanced spatial feature extraction, achieving **91% accuracy with SGD optimization**. Experiments span transfer learning baselines, attention mechanisms, and systematic optimizer comparisons. Work submitted to the **16th IEEE ICCCNT conference**.

---

## Repository Structure

```
├── dilation_CNN_6class_83pct.ipynb                       # Custom dilated CNN — 6-class, 83% (early run)
├── dilation_CNN_6class_83pct_v2.ipynb                    # Dilated CNN variant — refined architecture
├── optimizer_comparison_RMSprop_Adagrad_SGD_91pct.ipynb  # Optimizer comparison — SGD achieves 91%
├── optimizer_check_6class.ipynb                          # Optimizer sweep on dilated CNN
├── SGD_90pct.ipynb                                       # SGD-tuned dilated CNN — 90% checkpoint
├── TL_AD.ipynb                                           # VGG16 + VGG19 transfer learning baseline
├── transfer_learning_on_MRI.ipynb                        # Transfer learning on non-augmented data
├── augmentation/
│   └── data_augmentation.ipynb                           # Image augmentation pipeline for ADNI dataset
├── transfer_learning_models/
│   ├── VGG16.ipynb                                       # VGG16 fine-tuned — 84% accuracy
│   ├── DenseNet201.ipynb                                 # DenseNet201 fine-tuned — 82% val accuracy
│   ├── InceptionV3.ipynb                                 # InceptionV3 fine-tuned — 78% accuracy
│   ├── InceptionResNetV2.ipynb                           # InceptionResNetV2 fine-tuned — 81% accuracy
│   └── MobileNetV2.ipynb                                 # MobileNetV2 fine-tuned — 73% accuracy
└── attention/
    ├── attention_6class_undersampled.ipynb               # Attention model on undersampled 6-class data
    ├── attention_model.ipynb                             # MobileNet backbone with attention mechanism
    ├── attention_cnn_baseline.ipynb                      # Baseline attention CNN
    ├── attention_cnn_v2.ipynb                            # Attention CNN with VGG16 backbone
    └── optimizer_comparison.ipynb                        # SGD vs Adam across neuron configurations
```

## Dataset

ADNI (Alzheimer's Disease Neuroimaging Initiative) — MRI scans across six dementia severity stages.

## Key Results

| Model | Accuracy |
|---|---|
| Dilated CNN + SGD | **91%** |
| VGG16 (transfer learning) | 84% |
| InceptionResNetV2 | 81% |
| DenseNet201 | 82% val |
| InceptionV3 | 78% |
| MobileNetV2 | 73% |
