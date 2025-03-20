# Puzzle Solver / Occlusion Test

## Grid-based Occlusion

Inspired by: *Hide-and-Seek: A Data Augmentation Technique for Weakly-Supervised Localization and Beyond, Krishna Kumar Singh et al.*

### What We Did to the Images

To evaluate model robustness, we applied a grid-based occlusion technique to the images. This method involves randomly masking multiple small patches in an image using a grid structure. The goal is to simulate partial occlusions and test how well the model can still classify the images correctly.

The occlusion process works as follows:

1. The image is divided into a grid of fixed-size patches.
2. Each patch has a certain probability of being masked (i.e., set to zero).
3. This transformation is applied to both training and test images to assess the impact on model performance.

This approach helps us measure how robust a model is to missing information and whether retraining with occluded images improves its performance.

## Scores

#### First, we check the original model's behavior

*We use model weights, previously trained on pure images, to see robustness.*

$$
\text{Pure Model Robustness} = \frac{\text{Accuracy on occluded images}}{\text{Accuracy on non-occluded images}}
$$

After training on altered images, we see how the model improved.

$$
\text{Trained Model Robustness Improvement} = \frac{\text{New model accuracy on occluded images}}{\text{Old model accuracy on occluded images}}
$$

