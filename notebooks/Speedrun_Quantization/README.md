# SpeedRun Mode / Quantization

## PQT
Post-Training Quantization (PQT) is a technique to optimize deep learning models for faster inference and lower memory usage while maintaining accuracy. Instead of using full-precision 32-bit floating point numbers, we convert model weights and activations into more compact 8-bit integers. This significantly reduces computational cost and model size, making it ideal for edge devices and real-time applications.

### How We Did It
1. **Loaded a Pre-Trained Model** – We start with a trained model to avoid training from scratch.
2. **Defined Quantization Configuration** – Specify how activations and weights should be quantized using Observers eg. MinMax.
3. **Fused Layers** – Combine adjacent operations (e.g., convolution, batch normalization, and activation) to simplify computations and improve efficiency.
4. **Prepared the Model** – Added quantization observers to analyze activations and collect statistics during calibration.
5. **Ran Calibration Data** – Passed sample data through the model to determine optimal scaling factors for quantization.
6. **Converted the Model** – Replaced floating-point computations with their integer equivalents, finalizing the optimized model.

---

## The Scores (Explained)

### Accuracy Retention
Quantization often leads to slight accuracy degradation. To quantify this, we compare the accuracy of the quantized model to the original:

$$
\text{Accuracy Retention} = \left( \frac{\text{Quantized Accuracy}}{\text{Original Accuracy}} \right) \times 100
$$

If this value is close to 100%, it means the model retained most of its predictive power.

### Inference Speedup
Since quantized models use integer arithmetic instead of floating-point operations, they typically run faster. We measure this improvement as:

$$
\text{Inference Speedup} = \frac{\text{Original Inference Time}}{\text{Quantized Inference Time}}
$$

A higher value here indicates that the model is executing significantly faster.

### Overall Score
To balance accuracy and speed improvements, we compute an overall score:

$$
\text{Overall} = \frac{\text{Accuracy Retention}}{100} + \frac{\text{Inference Speedup}}{5}
$$

This provides a concise way to compare different quantization strategies.

---
