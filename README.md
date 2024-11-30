QR Code Generator
This project creates QR codes for any URL using Python. It includes examples for both basic and customized QR codes.

Features
Generate a simple QR code for a URL.
Customize QR code with foreground and background colors.
Save the QR code as a PNG image.
Requirements
Python 3.10 or higher
qrcode library
Pillow library
Installation
Install the required libraries:

bash
Copy code
pip install qrcode pillow
(Optional) Update pip to the latest version:

bash
Copy code
python -m pip install --upgrade pip
Usage
Generating a Basic QR Code
python
Copy code
import qrcode as qr

# Create a simple QR code
img = qr.make("https://www.linkedin.com/in/mohit-yavarna-967897264/")
img.save("mohit_linkedIN.png")
Generating a Customized QR Code
python
Copy code
import qrcode
from PIL import Image

# Create a QR code object with customization options
```qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=4
)```

# Add data to the QR code
qr.add_data("https://www.linkedin.com/in/mohit-yavarna-967897264/")
qr.make(fit=True)

# Customize colors
img = qr.make_image(fill_color="blue", back_color="white")
img.save("mohit_linkedin1.png")
Output
mohit_linkedIN.png: Basic QR code
mohit_linkedin1.png: Customized QR code with a blue foreground and white background.
Notes
The fill_color and back_color options can be adjusted to create QR codes with different color schemes.
Make sure the required libraries are installed before running the code.
Author
Mohit Yavarna
LinkedIn Profile
