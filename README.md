# Simple Image Captioning with BLIP and Gradio

This project demonstrates a simple image captioning application using the BLIP (Bootstrapping Language-Image Pre-training) model from Hugging Face's `transformers` library and a user-friendly web interface built with `gradio`.

## Overview

The application allows users to upload an image, and it will generate a textual caption describing the content of the image using the pre-trained BLIP model.

## Setup

### Prerequisites

* Python 3.6 or higher
* pip (Python package installer)

### Installation

1.  Clone the repository (if you have one):
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  Install the necessary Python libraries:
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You'll need to create a `requirements.txt` file with the following content if you don't have one yet):*
    ```
    gradio
    transformers
    Pillow
    torch
    ```

## Usage

1.  Run the Python script:
    ```bash
    python your_script_name.py
    ```
    *(Replace `your_script_name.py` with the actual name of your Python file containing the code).*

2.  Gradio will provide a local URL (usually starting with `http://127.0.0.1:`). Open this URL in your web browser.

3.  You will see a simple interface with an "Upload Image" area. Drag and drop an image or click to select one from your computer.

4.  Once the image is uploaded, the BLIP model will process it, and the generated caption will be displayed in the "Generated Caption" text box below the image.

## Code Explanation

The Python script performs the following steps:

* **Imports Libraries**: Imports necessary modules from `PIL`, `transformers`, `gradio`, and `torch`.
* **Loads Pre-trained Model**: Loads the BLIP model and its processor from the `"Salesforce/blip-image-captioning-base"` repository.
* **GPU Acceleration**: Checks for and utilizes a CUDA-enabled GPU if available to speed up the processing.
* **`generate_caption` Function**: This function takes an image as input, preprocesses it using the BLIP processor, generates a caption using the BLIP model, and decodes the output into a human-readable string.
* **Gradio Interface**: Creates a simple web interface with an image upload component and a text box to display the generated caption.
* **Launches the Interface**: Starts the Gradio web server, making the interface accessible in your browser.

## Example

Upon uploading an image of a cat, the generated caption might be something like:
