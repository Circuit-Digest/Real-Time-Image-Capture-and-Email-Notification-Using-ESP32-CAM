# 📸 ESP32-CAM Based Photo Capture and Photo Transfer

## 🚀 Capture and Email Images Using ESP32-CAM

This project demonstrates how to capture an image using the ESP32-CAM module and send it directly to an email address using WiFi and a secure HTTPS API.

The system allows real-time photo capture and instant email transfer, making it a powerful IoT-based monitoring solution.

---

## 🧠 Project Overview

The ESP32-CAM module connects to a WiFi network and initializes the onboard camera.

When a trigger event occurs (such as button press or motion detection), the ESP32-CAM:
1. Captures an image
2. Stores it in memory buffer
3. Sends the image via HTTPS request
4. The cloud API forwards the image to a registered email address

This creates a complete ESP32 CAM send picture email system.

---

## 🛠️ Components Required

| Component | Quantity |
|------------|----------|
| ESP32-CAM Module | 1 |
| Push Button |  2 |
| Breadboard | 1 |
| Connecting Wires | As required |

---
## ⚙️ Working Principle

1. ESP32-CAM connects to WiFi.
2. Camera module initializes successfully.
3. Image capture function is triggered.
4. Captured JPEG image is stored in frame buffer.
5. Secure HTTPS client is created.
6. Image is sent using POST request.
7. Email notification with image attachment is delivered.

---

## 🌐 ESP32 CAM Send Email Process

- Connect to WiFi network
- Create secure WiFiClientSecure object
- Prepare JSON/email API payload
- Attach captured image buffer
- Send HTTPS request
- Receive server response
- Email delivered successfully

---

## 🔐 Key Features

✔ Real-time image capture  
✔ Secure HTTPS communication  
✔ Email with image attachment  
✔ Low-cost IoT solution  
✔ WiFi-enabled photo transfer  
✔ Cloud API integration  

---

## 📄 Important Code Sections

### Include Required Libraries
```cpp
#include "esp_camera.h"
#include <WiFi.h>
#include <WiFiClientSecure.h>
```

### WiFi Setup
```cpp
const char* ssid = "YOUR_SSID";
const char* password = "YOUR_PASSWORD";
```

### Image Capture
```cpp
camera_fb_t * fb = esp_camera_fb_get();
```

### Sending Email
```cpp
client.println("POST /api/send-email HTTP/1.1");
```

---

## 📬 Applications

- Home Security System  
- Smart Door Monitoring  
- Visitor Capture System  
- IoT Surveillance  
- Industrial Monitoring  
- Wildlife Observation  

---

## 🔧 Troubleshooting

### Camera Initialization Failed
- Check power supply (5V 2A recommended)
- Verify camera model configuration
- Ensure correct pin mapping

### WiFi Not Connecting
- Check SSID and password
- Ensure strong signal
- Reset ESP32-CAM

### Email Not Received
- Verify API key
- Check HTTPS port
- Check spam folder

### Brownout Detector Error
- Use proper external 5V power supply
- Avoid powering from weak USB port

---

## 🔮 Future Enhancements

- Add PIR motion detection
- Add OLED status display
- Cloud storage integration
- Mobile app notification
- AI-based object detection
- Live video streaming

---

## 📚 Learning Outcomes

After completing this project, you will understand:

- ESP32-CAM camera initialization
- WiFi communication
- Secure HTTPS requests
- Image buffer handling
- Cloud API integration
- IoT-based email notification systems

---

## 📌 Conclusion

This ESP32-CAM Based Photo Capture and Photo Transfer project demonstrates how embedded systems can combine sensing, networking, and cloud communication to create intelligent real-time monitoring systems.

It is a practical and scalable IoT project suitable for both beginners and advanced developers.

---

