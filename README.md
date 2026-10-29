
Cross-Format Fidelity Assessment in Raw Ovarian DICOM Ultrasound Images

Overview
========

Digital Imaging and Communications in Medicine (DICOM) is a standard for storing medical images and associated metadata. Although DICOM supports interoperability across medical imaging systems, converting DICOM images into conventional image formats may introduce changes in pixel values, image quality, and clinically relevant information.

This project presents a systematic experimental framework for evaluating the effects of image format conversion on raw ovarian ultrasound DICOM images, including single-view, dual-view (left/right), and Color Doppler acquisitions.

The framework investigates image fidelity following conversion into grayscale, lossless, and lossy image formats using quantitative image quality metrics and pixel-level analysis.

DATASET AVAILABILITY:
===================

The experiments were conducted using retrospective ovarian ultrasound DICOM images obtained from a clinical source. The dataset contains private clinical imaging data and is not included in this repository.

In accordance with patient privacy requirements, ethical guidelines, and institutional data-sharing restrictions, the dataset is not publicly available. 

Image Quality Metrics
===================
The framework supports the following evaluation metrics:

PSNR
  Measures image reconstruction error on a logarithmic scale.
RMSE
  Quantifies the root mean square difference between pixel values.
SSIM
  Measures structural similarity between reference and converted images.
Histogram Correlation
  Evaluates the similarity between image intensity distributions.
Pixel Difference
  Identifies pixel-level changes introduced during conversion.
Changed Pixel Percentage
  Measures the proportion of pixels with differences.
RGB Channel Disparity
  Quantifies differences among the red, green, and blue channels.
Supported Image Formats
=====================
        TIFF
        PNG
        BMP
        JPEG
        MONOCHROME2

Requirements
============

The implementation uses Python and the following libraries:

NumPy

PyDICOM

pandas

Pillow

Matplotlib

scikit-image

Additional DICOM decompression plugins may be required depending on the transfer syntax of the input files.

Install the required dependencies:
================================

pip install numpy pydicom pandas Pillow matplotlib scikit-image

Limitations
============

Results may depend on the original DICOM encoding, photometric interpretation, and image content.

RGB-to-grayscale conversion can alter or remove color information relevant to Color Doppler imaging.

Lossy JPEG conversion may introduce compression artifacts.
