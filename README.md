GPU-Accelerated Image Processing Using CUDA

Overview

This project demonstrates GPU-accelerated image processing using NVIDIA CUDA. It implements a box blur algorithm that smooths grayscale images by averaging neighboring pixel values using parallel GPU computation.

Objectives

* Understand GPU programming with NVIDIA CUDA.
* Implement parallel image processing using CUDA kernels.
* Explore GPU memory management and thread organization.
* Learn how parallel computing can be applied to image processing.

Technologies Used

* Language: C++ with CUDA
* Platform: NVIDIA CUDA
* Algorithm: Box Blur
* Input Format: PGM grayscale image

How It Works

1. Load a grayscale image in PGM format.
2. Allocate memory on the GPU and transfer the image data.
3. Launch CUDA threads to process pixels in parallel.
4. Calculate average pixel intensities using neighboring pixels.
5. Copy the processed data back to the CPU.
6. Save the blurred image as an output file.

Project Structure

GPU-Accelerated-Image-Processing-Using-CUDA/
├── src/
│   └── box_blur.cu
├── samples/
│   └── sample.pgm
├── Makefile
├── run.sh
├── .gitignore
└── README.md

Requirements

* NVIDIA GPU compatible with your CUDA version
* NVIDIA CUDA Toolkit
* CUDA-compatible C++ compiler (nvcc)
* GNU Make

Build and Run

Build the project:

make

Run the image-processing program:

./box_blur samples/sample.pgm samples/blurred.pgm 1

The output image will be saved as samples/blurred.pgm, provided the program and paths are configured as shown.

Alternatively, if the included script supports these commands:

chmod +x run.sh
./run.sh

Expected Result

The program should generate a grayscale image with a blur effect applied to the original image. Successful execution depends on a working CUDA environment and compatible input files.

Applications

* Image smoothing and preprocessing
* Computer vision
* Medical image processing
* GPU parallel computing education
* Image analysis workflows

Future Improvements

* Compare CPU and GPU execution times.
* Process larger images.
* Experiment with different blur kernel sizes.
* Implement additional filters such as sharpening and edge detection.

Learning Outcomes

This project provides practical experience with CUDA kernels, GPU threads, memory allocation, host-to-device transfers, and parallel image processing.

Author

Sanskar Bhatkar

License

This project is intended for educational purposes.
