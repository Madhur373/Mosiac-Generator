# Mosiac-Generator
Here's a GitHub README template for a photo mosaic generator project using OpenCV:

---

# Photo Mosaic Generator

This project is a **Photo Mosaic Generator** built with **Python** and **OpenCV**. It creates a photo mosaic by dividing a large image into smaller tiles and replacing each tile with a smaller image that closely matches the color and pattern of that region. Perfect for generating artistic mosaics using any collection of images as tiles!

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## Features

- Converts any image into a photo mosaic.
- Supports a library of images for creating diverse mosaic patterns.
- Adjustable tile size for controlling mosaic detail.
- Color averaging for better matching of tile colors to the main image.

## Demo

![Photo Mosaic Example](demo/demo_mosaic.png)

## Requirements

- Python 3.6+
- [OpenCV](https://opencv.org/) (for image processing)
- [NumPy](https://numpy.org/) (for array manipulation)

Install the necessary packages:

```bash
pip install opencv-python numpy
```

## Installation

1. **Clone this repository**:

    ```bash
    git clone https://github.com/yourusername/photo-mosaic-generator.git
    cd photo-mosaic-generator
    ```

2. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare your images**:
   - Place all images to be used as tiles in a directory called `tiles/` (or any other folder of your choice).

2. **Run the generator**:
   - Use the following command to generate a mosaic:
   
    ```bash
    python mosaic_generator.py --input main_image.jpg --output mosaic_output.jpg --tiles_dir tiles/ --tile_size 30
    ```

   - Replace `main_image.jpg` with the path to the main image you want to convert into a mosaic, and `tiles/` with the path to your tile images folder.

### Command-Line Arguments

| Argument      | Description                                                |
|---------------|------------------------------------------------------------|
| `--input`     | Path to the main image.                                    |
| `--output`    | Path for saving the generated mosaic image.                |
| `--tiles_dir` | Directory containing the images to use as mosaic tiles.    |
| `--tile_size` | Size of each tile in pixels (e.g., 30 for 30x30 tiles).    |

## Project Structure

```
photo-mosaic-generator/
├── tiles/                # Directory of tile images (add your own)
├── demo/                 # Folder with demo images (optional)
├── mosaic_generator.py   # Main script for generating photo mosaic
├── requirements.txt      # Required Python packages
└── README.md             # Project documentation
```

## How It Works

1. **Tile Matching**:
   - Each tile in the main image is replaced by an image from the `tiles/` directory that closely matches the average color of that tile.
2. **Color Averaging**:
   - For each tile in the main image, the script calculates the average color and then searches the `tiles/` folder for an image with a similar color profile.

## Contributing

Contributions are welcome! Feel free to open issues or create pull requests.
