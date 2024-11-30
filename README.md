# QR Code Generator
This project creates QR codes for any URL using Python. It includes examples for both basic and customized QR codes.

## Features
1. Generate a simple QR code for a URL.
2. Customize QR code with foreground and background colors.
3. Save the QR code as a PNG image.
## Requirements
1. Python 3.10 or higher
2. qrcode library
3. Pillow library
## Installation
Install the required libraries:
```python
pip install qrcode pillow
```
```python
import qrcode as qr
```

## Create a simple QR code
```python
img = qr.make("https://www.linkedin.com/in/mohit-yavarna-967897264/")
img.save("mohit_linkedIN.png")
Generating a Customized QR Code
python
Copy code
import qrcode
from PIL import Image
```

## Create a QR code object with customization options
```python
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=4
)
```

## Add data to the QR code
```python
qr.add_data("https://www.linkedin.com/in/mohit-yavarna-967897264/")
qr.make(fit=True)
```
## Customize colors
```python
img = qr.make_image(fill_color="blue", back_color="white")
img.save("mohit_linkedin1.png")
```
### Output
mohit_linkedIN.png: Basic QR code![mohit_linkedin1](https://github.com/user-attachments/assets/e3cadda9-831c-4f11-8c7d-fe900f551c33)


mohit_linkedin1.png: Customized QR code with a blue foreground and white background.
![mohit_linkedIN](https://github.com/user-attachments/assets/51c18d28-4211-45e2-9103-fbce4fdf7921)

### Notes
The fill_color and back_color options can be adjusted to create QR codes with different color schemes.
Make sure the required libraries are installed before running the code.

### Author
- Mohit Yavarna
- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/mohit-yavarna-967897264/)

Thank you for your support, and I look forward to connecting with you!
