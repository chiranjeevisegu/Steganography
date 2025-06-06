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
