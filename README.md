# InSPyReNet Background Removal Wrapper

[![Open In Colab]([[https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/InSPyReNet_Background_Removal.ipynb](https://github.com/aler69/test/blob/main/InSPyReNet_Google_Colab_Notebook.ipynb)](https://github.com/aler69/test/blob/main/InSPyReNet%20Google%20Colab%20Notebook.ipynb))

A simple and efficient wrapper for the [InSPyReNet](https://github.com/plemeri/InSPyReNet) background removal model, optimized for Google Colab usage.

## Features

- 🚀 One-click Google Colab integration
- 🖼️ Support for various image formats
- 🎯 Easy-to-use wrapper class
- 📊 Visual results display
- 💾 Automatic model downloading
- 🔄 Batch processing capability
- 🎨 Transparent background output

## Quick Start

1. Click the "Open in Colab" button above
2. Run all cells in order
3. Upload your image when prompted
4. Get your result with transparent background!

## Requirements

All requirements are automatically installed when running the notebook:
- PyTorch
- torchvision
- PIL
- numpy
- matplotlib
- gdown

## Usage Example

```python
# Initialize the wrapper
wrapper = InSPyReNetWrapper()

# Process a single image
result = wrapper.remove_background('path/to/image.jpg')

# Save the result
wrapper.save_result(result, 'output.png')

# Get both result and mask
result, mask = wrapper.remove_background('path/to/image.jpg', return_mask=True)
```

## Local Installation

If you want to run this locally instead of Colab:

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

2. Clone InSPyReNet and download the model:
```bash
git clone https://github.com/plemeri/InSPyReNet.git
pip install gdown
gdown --id 1qw1TGadiNHPKJ9MwCTgOrRKNIdrsxVsP -O InSPyReNet/saved_models/isnet.pth
```

3. Install requirements:
```bash
pip install torch torchvision pillow numpy matplotlib
```

## Model Details

This wrapper uses the InSPyReNet model with the following specifications:
- Input size: 384x384 (automatically resized)
- Output: RGBA image with transparent background
- GPU support with automatic device selection

## Contributing

Feel free to open issues or submit pull requests for any improvements!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Original InSPyReNet implementation by [plemeri](https://github.com/plemeri)
- Based on the paper "InSPyReNet: Stepped Progressive Refinement Network for Background Removal"

## Note

Before using the "Open in Colab" button:
1. Replace `YOUR_USERNAME` with your GitHub username
2. Replace `YOUR_REPO_NAME` with your repository name
3. Make sure your notebook is named `InSPyReNet_Background_Removal.ipynb` and is in the root directory of your repository
