# Real_colorization_video
# 🎬 TASK 6: Real-Time Video Colorization (Custom Models)

## 👩‍💻 Author
**Mehkaan Anjum**

## 🏢 Company
**Elevance Skills**

---

## 📌 Project Description

This project performs **real-time grayscale video colorization** using three custom algorithm-based models.

Unlike predefined OpenCV colormaps or AI pretrained models, this system manually generates RGB channels using mathematical transformations on grayscale intensity values.

The system:
- Uploads a grayscale video
- Processes it frame-by-frame
- Applies selected custom color model
- Saves the final colorized video
- Downloads the output automatically

---

## 🚀 Features

✅ Real-time video processing  
✅ 3 Custom colorization models  
✅ Frame-by-frame transformation  
✅ Live preview during execution  
✅ Automatic output download  
✅ Google Colab compatible  

---

## 🧠 Working Algorithm

1. Upload grayscale video.
2. Capture video using `cv2.VideoCapture()`.
3. Extract FPS, width, height.
4. Convert each frame to grayscale.
5. Normalize grayscale values (0 to 1).
6. Apply selected colorization model.
7. Merge RGB channels.
8. Save output using `cv2.VideoWriter`.
9. Download final MP4 file.

---

## 🎨 Custom Colorization Models

### 1️⃣ Warm Tone Model
Creates warm reddish-yellow effect.

```python
red   = (norm * 255).astype(np.uint8)
green = (norm * 180).astype(np.uint8)
blue  = (norm * 100).astype(np.uint8)
```

✔ High Red  
✔ Medium Green  
✔ Low Blue  

---

### 2️⃣ Cool Tone Model
Creates bluish cold atmosphere effect.

```python
red   = (norm * 100).astype(np.uint8)
green = (norm * 180).astype(np.uint8)
blue  = (norm * 255).astype(np.uint8)
```

✔ High Blue  
✔ Medium Green  
✔ Low Red  

---

### 3️⃣ Cinematic Model
Creates dramatic movie-style grading.

```python
red   = (np.sqrt(norm) * 255).astype(np.uint8)
green = (norm * 150).astype(np.uint8)
blue  = ((1 - norm) * 200).astype(np.uint8)
```

✔ Non-linear Red boost  
✔ Moderate Green  
✔ Inverted Blue mapping  

---

## 📂 Workflow Diagram

```
Upload Video
      ↓
Read Frame
      ↓
Convert to Grayscale
      ↓
Normalize Pixel Values
      ↓
Apply Selected Model
      ↓
Merge RGB Channels
      ↓
Write Output Video
      ↓
Download File
```

---

## 🛠️ Technologies Used

- Python
- OpenCV
- NumPy
- Google Colab
- Video Processing Techniques

---

## 📦 Installation (Colab)

```python
!pip install -q opencv-python-headless
```

---

## ▶️ How to Run

1. Open Google Colab.
2. Paste full Python code.
3. Run the cell.
4. Upload grayscale video.
5. Choose model (1 / 2 / 3).
6. Wait for processing.
7. Output video downloads automatically.

---

## 📊 Output Details

- Output File: `real_time_colorized_output.mp4`
- Format: MP4
- Resolution: Same as input
- FPS: Same as input

---

## 🔐 Safety & Compliance

- No pretrained AI models used
- No external datasets required
- Fully algorithm-based
- Academic safe
- Internship submission ready

---

## 💡 Applications

- Black & white video enhancement
- Educational image processing demo
- Video editing effects
- Algorithm learning project

---

## 📜 Conclusion

This project demonstrates real-time grayscale video colorization using mathematical RGB transformations instead of predefined colormaps or AI models.

It improves understanding of:

- Frame-by-frame video processing
- Pixel normalization
- RGB channel manipulation
- Algorithm-based color generation
- Video writing and exporting

The system is lightweight, efficient, and suitable for academic and internship submission.

---

⭐ If you like this project, give it a star on GitHub!
