# ADAS_Object_Detection_YOLOv8
This project implements Advanced Driver Assistance System (ADAS) object detection using YOLOv8, a state-of-the-art real-time object detection model. The model is trained and tested on the COCO-128 dataset, identifying objects such as cars, pedestrians, traffic lights, and road signs to improve vehicle safety.

Key Features:

📌 Trained YOLOv8 on the COCO-128 dataset for ADAS applications

🎯 Tested detection on 4 selected images (Urban road, Airplane, Traffic scene)

🔍 Flowchart & Explanation of ADAS Workflow

📊 Results saved for visualization & further analysis


📦 ADAS_Object_Detection_YOLOv8  
 ┣ 📜 ADAS_Object_Detection_YOLOv8.ipynb  # Kaggle Notebook (Main Project)  
 ┣ 📜 dataset.yaml                       # Dataset configuration  
 ┣ 📂 runs/detect/                        # YOLOv8 Training Results  
 ┣ 📂 ADAS_results/                        # Final detected images  
 ┣ 📜 README.md                           # Project Documentation  
 ┣ 📜 requirements.txt                     # Dependencies  


Dataset Information
📂 Dataset: COCO-128

🏷 Classes Detected: Car, Pedestrian, Traffic Light, Stop Sign, Airplane, etc.

🖼 Images Used for Testing:

✅ Urban Road Scene

✅ Airplane Image

✅ Traffic Scene (Vehicles, Signs)

✅ Additional Road Scene

Model Training & Testing

 Training YOLOv8

  ```from ultralytics import YOLO
model = YOLO("yolov8n.pt")
model.train(data="dataset.yaml", epochs=50, imgsz=640)```


Object Detection on Test Images
```results = model.predict(source="/kaggle/input/coco128/coco128/images/train2017/000000000349.jpg", save=True, conf=0.2)```

Displaying Results
```from PIL import Image
from IPython.display import display
display(Image.open("runs/detect/predict/000000000349.jpg"))```


📌 Final Results
🚗 YOLO successfully detected ADAS-related objects! ✅
📂 All images & detections are saved in ADAS_results/
📝 Project Report & Flowchart included for detailed analysis

