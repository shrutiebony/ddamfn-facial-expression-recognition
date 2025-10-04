# ddamfn-facial-expression-recognition
#### Research Paper: https://arxiv.org/pdf/2407.12390
#### Medium Article: https://medium.com/@shrutiebony/enhancing-facial-expression-recognition-with-dual-direction-attention-networks-7be155dbfacc
#### Slide Deck Link: https://www.slideshare.net/slideshow/enhancing-facial-expression-recognition-with-ddamfn-pptx/273746973
#### Youtube Video: https://www.youtube.com/watch?v=tfccY5c5RJA

## Abstract
This project builds on the Dual-Direction Attention Mixed Feature Network (DDAMFN) architecture to improve facial expression recognition for the 7th ABAW Challenge at ECCV 2024. By leveraging multitask learning, the network simultaneously predicts:

Valence-Arousal scores,
Emotion categories (happiness, sadness, anger, etc.), and
Facial Action Units (AUs) detection.
The DDAMFN architecture employs attention mechanisms and mixed feature extraction techniques to enhance the representation of subtle facial expressions in real-world scenarios ("in-the-wild" datasets).




## Features
### Dataset Curation
Dataset: A subset of the Aff-Wild2 dataset (s-Aff-Wild2) provided for the 7th ABAW Challenge.
Annotation Filtering: Strict curation was applied to remove invalid annotations. Frames containing annotation values outside acceptable ranges were excluded.
Final dataset details:
Training: 52,154 frames
Validation: 15,440 frames

## Network Architecture
The model builds on:

MobileFaceNet (MFN) for feature extraction.
Dual-Direction Attention Module (DDA): A dual-head attention mechanism to enhance context learning.
Global Depthwise Convolution (GDConv): Captures intricate spatial dependencies.
Three Task-Specific Heads:
Valence-Arousal Head: Predicts 2 values.
Emotion Recognition Head: Predicts 8 emotion categories.
Action Unit Head: Predicts 12 discrete facial muscle movements.

## Evaluation Metrics
Accuracy for discrete tasks (Emotion Recognition, Action Units).
Concordance Correlation Coefficient (CCC) for continuous tasks (Valence-Arousal).
Comparison against baseline methods provided by the ABAW challenge.

