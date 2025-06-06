🖼️ Image Steganography
This project implements an image steganography system to securely hide secret text messages inside digital images using LSB substitution and Discrete Wavelet Transform (DWT). The hidden data is imperceptible and can be extracted only by the intended recipient.

🔍 Features
-Embed secret text into digital images
-Supports LSB and DWT-based embedding techniques
-Minimal distortion in the stego image
-Reliable message extraction from received images
-Compatible with PNG, BMP, and JPEG formats

🧪 Methodology Summary
Step 1: Preprocessing
-Input: Digital image
-Technique: Resize and standardize format (e.g., convert to PNG)
-Purpose: Ensure consistent dimensions and color format (typically RGB)

Step 2: Message Encoding
-Input: Secret text
-Technique: ASCII to binary conversion
-Purpose: Represent the message in binary form for embedding

Step 3: Data Embedding
-Input: Cover image
-Techniques:
-LSB substitution: Replace least significant bits of pixel values with message bits
-DWT embedding: Hide data in wavelet coefficients
-Purpose: Hide message while maintaining visual quality

Step 4: Stego Image Transmission
-Transmit the stego image through a secure or public channel

Step 5: Data Extraction
-Input: Stego image
-Techniques: Inverse LSB or DWT
-Purpose: Extract binary message and decode to retrieve original text

💻 Tech Stack
| Component       | Technology             |
| --------------- | ---------------------- |
| Language        | Python 3.x             |
| Image Handling  | OpenCV / PIL           |
| DWT Processing  | PyWavelets (`pywt`)    |
| Binary Encoding | Standard ASCII & UTF-8 |
| Evaluation      | PSNR, SSIM (skimage)   |



🎥 Video Steganography
This project implements a steganography system that hides secret data (text, image, or file) within a video file. It uses frame-wise encoding techniques like LSB (Least Significant Bit) and optionally integrates AES encryption for enhanced security.

🔍 Features
Embed and extract hidden data in videos (MP4, AVI, etc.)

Supports text, image, or file-based payloads

Uses LSB or DCT/DWT-based techniques

Preserves original audio and video quality

Optional AES encryption for secure data hiding

Performance evaluation via PSNR and SSIM

🧪 Methodology Summary
1.Preprocessing
-Extract frames from video
-Convert secret data to binary or hexadecimal

2.Data Embedding
-Modify pixel values or frequency components
-Optionally encrypt data before embedding

3.Video Reconstruction
-Combine modified frames and restore audio

4.Data Extraction
-Decode hidden bits and reconstruct original data

💻 Tech Stack
| Component      | Technology           |
| -------------- | -------------------- |
| Language       | Python 3.x           |
| Video Handling | OpenCV, FFmpeg       |
| Numerical Ops  | NumPy                |
| Image I/O      | PIL / OpenCV         |
| Audio Handling | moviepy (optional)   |
| Encryption     | `pycryptodome` (AES) |
| Evaluation     | PSNR, SSIM (skimage) |
