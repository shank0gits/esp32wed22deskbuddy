# ESP32-S3 Smart AI Weather Display

A futuristic ESP32-S3 based smart display with:

* Animated AI Eyes 👀
* Real-time Weather 🌦️
* Forecast 📅
* Clock & World Clock 🕒
* Mood Based Animations 😄
* Touch Controls ✨
* OLED Display UI 📱

Built using ESP32-S3 Zero + SH1106 OLED.

---

# 📦 Features

## 👀 Animated AI Eyes

* Smooth spring physics motion
* Blinking animation
* Mood expressions
* Pupil tracking
* Idle eye movement

## 🌦️ Weather System

* Current weather
* Feels like temperature
* Humidity
* Weather condition icons
* 3-Day forecast

## 🕒 Smart Clock

* NTP internet clock
* World clock
* Date display

## ✨ Touch Controls

| Action     | Function          |
| ---------- | ----------------- |
| Single Tap | Change Page       |
| Double Tap | Brightness Toggle |
| Long Press | Extra Features    |

---

# 🛠️ Hardware Required

| Component                        | Quantity |
| -------------------------------- | -------- |
| ESP32-S3 Zero                    | 1        |
| SH1106 OLED Display (128x64 I2C) | 1        |
| Touch Sensor / Push Button       | 1        |
| Jumper Wires                     | Some     |
| USB Cable                        | 1        |

Optional:

* VC-02 Voice Module
* Speaker
* I2S Amplifier
* Microphone

---

# 🔌 Wiring Connections

## OLED Display

| OLED Pin | ESP32-S3 Pin |
| -------- | ------------ |
| VCC      | 3.3V         |
| GND      | GND          |
| SDA      | GPIO 7       |
| SCL      | GPIO 8       |

## Touch Sensor

| Touch Pin | ESP32-S3 Pin |
| --------- | ------------ |
| OUT       | GPIO 9       |
| VCC       | 3.3V         |
| GND       | GND          |

---

# 💻 Arduino IDE Setup

## 1. Install Arduino IDE

Download Arduino IDE:

[https://www.arduino.cc/en/software](https://www.arduino.cc/en/software)

---

## 2. Install ESP32 Board Package

### Open:

Arduino IDE → File → Preferences

### Add this URL in:

Additional Board Manager URLs

```
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```

### Then:

* Go to Tools → Board → Boards Manager
* Search:

```
ESP32
```

* Install by Espressif Systems

---

# ⚙️ Board Upload Settings

## IMPORTANT SETTINGS

| Setting          | Value                   |
| ---------------- | ----------------------- |
| Board            | ESP32S3 Dev Module      |
| USB CDC On Boot  | Enabled                 |
| CPU Frequency    | 240MHz                  |
| Flash Mode       | QIO 80MHz               |
| Flash Size       | 4MB                     |
| Partition Scheme | Default 4MB with SPIFFS |
| PSRAM            | Disabled                |
| Upload Speed     | 921600                  |
| Port             | Select COM Port         |

---

# 📚 Required Libraries

Install these libraries from Arduino Library Manager:

## Required Libraries

* Adafruit GFX Library
* Adafruit SH110X
* Arduino_JSON

---

# 🌐 WiFi Configuration

Inside code edit these:

```cpp
wifiSsid = "YOUR_WIFI_NAME";
wifiPass = "YOUR_WIFI_PASSWORD";
```

---

# ☁️ Weather API Setup

## OpenWeatherMap API

1. Create account:
   [https://openweathermap.org/](https://openweathermap.org/)

2. Generate API Key

3. Replace inside code:

```cpp
apiKey = "YOUR_API_KEY";
```

---

# 🌍 City Configuration

Edit these values:

```cpp
city = "Farrukhabad";
countryCode = "IN";
```

Example:

```cpp
city = "Delhi";
countryCode = "IN";
```

---

# 🕒 Timezone Setup

Example:

```cpp
tzString = "IST-5:30";
```

---

# 🚀 Uploading the Code

## Steps

1. Connect ESP32-S3 using USB cable
2. Select correct COM Port
3. Click Upload
4. If upload fails:

   * Hold BOOT button
   * Press RESET once
   * Release BOOT after upload starts

---

# 📱 Pages Overview

| Page   | Description      |
| ------ | ---------------- |
| Page 1 | Animated AI Eyes |
| Page 2 | Digital Clock    |
| Page 3 | Weather Card     |
| Page 4 | World Clock      |
| Page 5 | Forecast Page    |

---

# 🎭 Mood System

| Mood    | Trigger          |
| ------- | ---------------- |
| Happy   | Clear Weather    |
| Sad     | Rain             |
| Sleepy  | Cold Temperature |
| Excited | Hot Temperature  |
| Angry   | Manual Mode      |
| Love    | Manual Mode      |

---

# 🔋 Future Upgrade Ideas

* Voice Assistant
* Alexa Style Web Search
* VC-02 Voice Commands
* Speaker Output
* AI Chat Responses
* Local Memory System
* Face Tracking
* Home Automation

---

# 🧠 Planned Voice Assistant System

Future upgrade architecture:

```text
VC-02 Voice Input
        ↓
ESP32-S3 Processing
        ↓
Online Search API
        ↓
OLED + Voice Response
```

---

# 🛠️ Troubleshooting

## OLED Not Working

* Check I2C wiring
* Verify SDA/SCL pins
* Confirm OLED address = 0x3C

## WiFi Not Connecting

* Check SSID/password
* Ensure 2.4GHz WiFi

## Upload Failed

* Use good USB cable
* Press BOOT while uploading
* Install correct drivers

## Weather Not Updating

* Check internet connection
* Verify API key

---

# 📸 Project Preview

Features included:

* Smooth animated eyes
* Dynamic emotions
* Real-time weather
* Clock system
* OLED UI
* Smart interactions

---

# ❤️ Credits

Developed using:

* ESP32-S3
* Arduino IDE
* OpenWeatherMap API
* Adafruit Libraries

Inspired by futuristic AI assistant designs.

---

# 📄 License

This project is open-source.
You can modify and improve it for personal learning and projects.

---

# ⭐ Support

If you like this project:

* Star the repository
* Share with friends
* Improve and build your own AI assistant

🔥 Happy Making!
