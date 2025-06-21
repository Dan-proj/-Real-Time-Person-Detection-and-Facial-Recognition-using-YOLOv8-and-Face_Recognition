# **Real-Time-Person-Detection-and-Facial-Recognition-using-YOLOv8-and-Face_Recognition**
This project integrates YOLOv8 object detection with facial recognition to identify and label known individuals in real-time from a webcam feed. It detects people using YOLOv8 and matches detected faces with known identities using the face_recognition library.
Here’s a clean and complete GitHub **title and project description** for your Python code using YOLOv8 and face recognition:

---
**🚀 Features:**

* Detects **persons only** using YOLOv8 (`yolov8n.pt` or `yolov8s.pt`)
* Recognizes and labels known faces using `face_recognition`
* Real-time detection via webcam
* Draws bounding boxes and displays names
* Shows “Unknown” for unmatched faces

**📦 Dependencies:**

* `ultralytics` (YOLOv8)
* `face_recognition`
* `opencv-python`
* `dlib`
* `numpy`

Install via pip:

```bash
pip install ultralytics face_recognition opencv-python
```

**🖼 How It Works:**

1. YOLOv8 detects all objects in the video stream.
2. Filters out only those with class ID 0 (`person`).
3. Crops each detected person box and performs facial recognition.
4. Matches with known encodings and labels them accordingly.

** 📁 Setup:**

* Add images of known people to your project directory.
* Encode their faces like:

```python
img = face_recognition.load_image_file('person.jpg')
encoding = face_recognition.face_encodings(img)[0]
known_face_encodings.append(encoding)
known_face_names.append("Person Name")
```

**💡 Notes:**

* Replace `'yolov8n.pt'` with `'yolov8s.pt'` or higher for better accuracy.
* Ensure proper lighting for better face detection.
* Press **`q`** to quit the webcam stream.

---
