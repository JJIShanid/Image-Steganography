# 🖼️ Image Steganography

A simple and effective Python-based **Image Steganography** tool that allows you to **hide secret messages inside images** and retrieve them later using **Least Significant Bit (LSB) encoding**.

---

## 📌 Features

- 🔐 Encode (hide) secret text messages in images
- 🔓 Decode (extract) hidden messages from stego-images
- 🖼️ Supports PNG and BMP images (lossless formats)
- 🧠 Uses LSB (Least Significant Bit) algorithm
- 🎯 Simple GUI (Tkinter) or CLI interface (based on your project)
- 💡 Useful for digital watermarking, secret messaging, and learning steganography

---

## 🛠️ Technologies Used

- **Python 3.x**
- `Pillow` – for image processing
- `Tkinter` – for GUI (if applicable)
- `argparse` – for CLI options (if applicable)

---

## 📂 Project Structure

```bash
Image-Steganography/
│
├── encode.py         # Script to encode text into an image
├── decode.py         # Script to decode text from an image
├── gui.py            # (Optional) GUI version using Tkinter
├── requirements.txt  # Python dependencies
├── README.md         # Project documentation
└── samples/
    ├── input.png     # Sample input image
    └── output.png    # Output image with hidden message
🚀 Getting Started
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/JJIShanid/Image-Steganography.git
cd Image-Steganography
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
Or manually:

bash
Copy
Edit
pip install pillow
🔐 Encode a message into an image
bash
Copy
Edit
python encode.py --input input.png --output output.png --message "This is a secret message!"
Parameters:
--input: Path to the source image

--output: Path to save the image with hidden message

--message: The secret text to hide

🔓 Decode the hidden message
bash
Copy
Edit
python decode.py --input output.png
It will extract and print the hidden message.

🧪 Example
🔐 Encoding:
bash
Copy
Edit
python encode.py --input samples/input.png --output samples/output.png --message "Hello Ishan!"
🔓 Decoding:
bash
Copy
Edit
python decode.py --input samples/output.png
Output:

yaml
Copy
Edit
Decoded Message: Hello Ishan!
📸 GUI Version (Optional)
If you have a gui.py file for a graphical interface:

bash
Copy
Edit
python gui.py
📖 How It Works
This project uses the Least Significant Bit (LSB) technique, where each pixel's RGB value is slightly altered to embed binary data. These small changes are visually undetectable.

For example:

Original Red Value: 11100110

After LSB embedding: 11100111 → only the last bit changes

✅ Limitations
Works best with lossless image formats (like .png)

Message size depends on image dimensions

Does not support image compression after embedding

📄 License
This project is licensed under the MIT License.

🙌 Acknowledgements
Inspired by cryptography and digital privacy techniques

Educational use for security, steganography, and Python learners

✍️ Author
Ishan JJIShanid
