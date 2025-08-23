# Contrastive Learning for Image Similarity

## Overview - What can be learnt from a single image?
This project uses PyTorch to train a ResNet-18 model with contrastive learning to compute image similarity from a single image. It includes image preprocessing, augmentation, model training, and similarity evaluation using Euclidean distance.

## Features
- Preprocesses and augments images from a single image using OpenCV and Albumentations.
- Trains a ResNet-18 model with contrastive loss to learn 128D embeddings.
- Compares a query image to others from the test data using various similarity metrics.
- Visualizes sorted comparison images by similarity/distance.


## Key Components
- **Augmentation**: Applies geometric, color, noise, and occlusion transformations.
- **Model**: ResNet-18 with a projection head, trained with contrastive loss.
- **Evaluation**: Computes 128 vector embeddings and sorts images by Euclidean distance.

## Usage Notes
- Replace `jcsmr.jpg` and `school4.jpeg` with your images.
- Adjust hyperparameters (`BATCH_SIZE`, `EPOCHS`, `LEARNING_RATE`) as needed.
- Change `similarity_metric` for other metrics (e.g., cosine, Manhattan).
- Uses GPU if available, else CPU.

## Limitations
- Trained on a single image with augmentations, limiting generalization.
- Assumes RGB images with `.png`, `.jpg`, or `.jpeg` extensions.

## License
MIT License.