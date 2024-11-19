# Neural Style Transfer and Stable Diffusion for Image Processing

This project explores advanced image processing techniques using **Neural Style Transfer** and **Stable Diffusion** to create visually stunning results by combining content and artistic styles.

---

## Overview

### Neural Style Transfer
Neural Style Transfer combines the **content** of one image with the **style** of another using pre-trained deep learning models.  
**Key Concepts**:
- **Content Image:** The structure and details of this image are retained.
- **Style Image:** The visual patterns, colors, and textures of this image are applied to the content.

Framework: **TensorFlow** and **TensorFlow Hub**.

---

### Stable Diffusion
Stable Diffusion is used for generating stylized images from text prompts and base images.  
**Key Features**:
- Transform images using pre-trained diffusion models.
- Modify artistic styles with simple prompts.

Framework: **PyTorch** and **Hugging Face Diffusers**.

---

## Objectives
1. Apply **Neural Style Transfer** to blend content and style images into new artistic outputs.
2. Utilize **Stable Diffusion** to generate stylized images based on text prompts.
3. Explore advanced loss functions (e.g., Style Loss, Content Loss, and Total Variation Loss).
4. Visualize intermediate and final results.

---

## Project Workflow

### Neural Style Transfer

1. **Input Images**:
   - Content Image: `vpkhoa.jpg`
   - Style Image: `Starry Night.jpg`

2. **Implementation**:
   - Use TensorFlow Hub to load a pre-trained style transfer model.
   - Extract style and content features using VGG19 layers.
   - Compute loss functions for style, content, and total variation to optimize the final stylized image.

3. **Optimization**:
   - Custom training loop with Adam optimizer.
   - Iteratively refine the output by minimizing the combined loss.

4. **Edge Detection**:
   - Use Sobel filters and high-pass filters for visualization.
   - Explore gradient changes in styled images.

5. **Output**:
   - Final output saved as `vpkhoa_output.png`.

---

### Stable Diffusion

1. **Setup**:
   - Load the `Stable Diffusion v1.5` model using Hugging Face Diffusers.
   - Use a pre-trained pipeline for image-to-image generation.

2. **Input**:
   - Base Image: `vpkhoa.jpg`.
   - Prompt: `"Van Gogh style"`

3. **Inference**:
   - Use the diffusion pipeline to transform the image into a new artistic style.
   - Modify parameters like strength and guidance scale for fine-tuning.

4. **Output**:
   - Final output saved as `vpkhoa_out.jpg`.

---

## Usage
### Neural Style Transfer
1. Load Input Images:
- Place the content image (vpkhoa.jpg) and style image (Starry Night.jpg) in the working directory.
2. Run the Script:
3. Output:
- The styled image will be saved as vpkhoa_output.png.
### Stable Diffusion
1. Set Up Model:
- Ensure the Stable Diffusion v1.5 model is downloaded.
2. Run the Script:
3. Output:
The stylized image will be saved as vpkhoa_out.jpg.

---

## Results
### Neural Style Transfer
- Combines the details of the content image with the artistic style of Starry Night.
- Demonstrates high-quality style transfer through optimization.
### Stable Diffusion
- Stylizes the content image based on the "Van Gogh style" prompt.
- Outputs vivid and creative transformations.

---

## Key Features
### Style Loss and Content Loss:
- Custom loss functions ensure balance between content and style.
### Edge Detection:
- Visualizes gradients and edges to evaluate stylization effects.
### Total Variation Loss:
- Smooths the output by reducing high-frequency artifacts.