# Smart Tracker

An AI-powered food recognition and monitoring system designed for restaurant refrigerators. This project uses YOLOv5s running on a Raspberry Pi to detect food and other stored items in real time, track how long they've been inside, estimate quantity, and send alerts when perishable limits or stock thresholds are reached.

# Features

- Real-time object detection via Pi Camera
- Custom-trained YOLOv5s model on restaurant-specific items (e.g. fruits, meat, drinks, utensils)
- Item presence tracking with perishable timers
- Quantity estimation using bounding box accumulation
- Optional alerts for low stock or expired items
- Lightweight Firebase integration for cloud logging and notifications (optional)

# System Requirements

- Raspberry Pi 4 (4GB+ recommended)
- Pi Camera Module (v2 or HQ)
- MicroSD card (16GB+)
- Python 3.7+
- Optional: LED strip for fridge lighting
- Optional: Firebase credentials (for cloud sync)

## AI Model

- **Model:** YOLOv5s (Ultralytics)
- **Framework:** PyTorch
- **Input Size:** 640x640
- **Dataset:** Custom dataset of labeled restaurant items
- **Training:** Requires ~100 labeled images per class for 90%+ accuracy
- **Output:** Label, bounding box, confidence score

{
"meat_01": {
"type": "meat",
"added": "2025-07-14T15:32:18",
"volume": 14320
}
}
