# Image-Thresholding
Image Thresholding
import cv2
import numpy as np

def image_thresholding(image_path):
    image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)
    _, thresholded = cv2.threshold(image, 128, 255, cv2.THRESH_BINARY)

    cv2.imshow('Thresholded Image', thresholded)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Example usage
image_path = 'path/to/your/image.jpg'
image_thresholding(image_path)
