# IoT-HospitalManagementsystem
Smart Hospital IoT System integrating Parking, Waste Management, Disaster Monitoring, Room Comfort, and Attendance with NodeMCU, Arduino, Raspberry Pi, and Firebase. 

# Smart Hospital IoT System

An advanced IoT-based Smart Hospital Management System integrating multiple subsystems for automation, monitoring, and safety.  
Built using NodeMCU, Arduino UNO, Raspberry Pi 4, Firebase Realtime Database, and a Mobile Dashboard.

---

# Features

 1. Smart Parking (NodeMCU1)
- Detects available/occupied slots using ultrasonic sensors.
- Automatic gate control with servo motor.
- Indicator LEDs for slot availability.
- Data synced with Firebase for real-time parking updates.

 2. Smart Waste Management (NodeMCU2 / Arduino Integration)
- IR sensor for object detection.
- Moisture sensor for wet/dry waste classification.
- Ultrasonic sensor for bin fill level.
- Automatic sorting with servo motor.
- Bin full alert via Firebase & dashboard.

 3. Disaster Monitoring (NodeMCU3)
- Flame sensor, Gas sensor (MQ135), and Vibration sensor (SW-420).
- Buzzer & Red LED alert system.
- Alerts pushed to Firebase & Mobile App.

 4. Room Comfort Monitoring (Arduino UNO → Raspberry Pi)
- DHT11 for temperature & humidity.
- MQ135 for air quality.
- PIR motion sensor to detect occupancy.
- White LED turns ON automatically when someone enters.

 5. RFID Attendance System (Raspberry Pi 4 + RC522)
- RFID reader (RC522) connected via SPI.
- Reads student/staff IDs and logs attendance to Firebase.
- Real-time logs accessible in dashboard.

---

# System Architecture

- Controllers: 3 × NodeMCU, 1 × Arduino UNO, 1 × Raspberry Pi 4
- Cloud: Firebase Realtime Database
- Communication: Wi-Fi (WPA2, HTTPS), Serial (Arduino → RPi)
- Dashboard: Web & Mobile App

---

## 🔐 Security Architecture

- Edge Security: Input validation & device authentication keys.  
- Network Security: WPA2 encryption, static IP, MAC/IP whitelisting.  
- Cloud Security: Firebase Authentication, Firestore access rules, AES encryption (at rest).  
- User Roles: Admin vs Staff with different dashboard privileges.  

---

## 📊 Dashboard & Mobile App

Web Dashboard  
  - View live sensor data.  
  - Access attendance logs.  
  - Monitor alerts.  
  - Analytics (via Firebase).  

Mobile App  
  - View real-time room status.  
  - Book parking slots.  
  - Receive emergency alerts.  
  - Monitor bin status & air quality.  



