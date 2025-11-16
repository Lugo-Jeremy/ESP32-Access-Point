# Cybersecurity : CSN150
Project: ESP32 Access Point

## Purpose
Set up ESP32 and Arduino enviornment. Execute sketch "Access Point". 

## Equipment
* [ESP32Cam](https://www.amazon.com/Aideepen-ESP32-CAM-Bluetooth-ESP32-CAM-MB-Arduino/dp/B08P2578LV/ref=sr_1_3?crid=4FY0ECFW0ZX7&keywords=ESP32+Cam&qid=1678902050&sprefix=esp32+cam%2Caps%2C240&sr=8-3)

* [USB Micro Data Cable](https://www.amazon.com/AmazonBasics-Male-Micro-Cable-Black/dp/B0711PVX6Z/ref=sr_1_1_sspa?keywords=micro+usb+data+cable&qid=1678902214&sprefix=Micro+USB+data+%2Caps%2C89&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFaU0NaUVZHU1RFUlAmZW5jcnlwdGVkSWQ9QTA3NTA4MDVFVERCS01HVlgxM1YmZW5jcnlwdGVkQWRJZD1BMDE4NTE1NTIwWUdONkdWSzU1M1Amd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)

## Links to documentation and tools

##### Video 1: 

##### Other Links: https://randomnerdtutorials.com/esp32-cam-access-point-ap-web-server/ 

##### AI GPTs used

## Steps I followed
1. Open Web Source to follow steps to set up access point for ESP32
2. Connect my ESP32 Cam with USB-C cable and open Arduino IDE
3. In Arduino IDE, go to File > Examples > ESP32 > Camera > CameraWebServer
4. Modify the SSID and password for the access point, I copied the same SSID and password from web source
5. I removed the following lines from the script: WiFi.begin(ssid, password);
while (WiFi.status() != WL_CONNECTED) {
  delay(500);
  Serial.print(".");
}
Serial.println("");
Serial.println("WiFi connected");
6. I then added WiFi.softAP (ssid, password); to the code.
7. The code is set up for the access point to work, I uploaded the code to run
8. Noticed that the code was not running properly, searched on Google how to set up access point for ESP32
9. There was a sample C++ code to copy for set up.
10. I copy and pasted the code, uploaded to run
11. The access point works properly, I was able to connect to the access point on my ESP32-CAM




## Final Report:
The access point was successfully set up using the Arduino IDE software for my ESP32-CAM. I originally was using the example that the Arduino IDE gave for reference and edited the ssid and password. The upload was successful but for some reason the access point was not showing up in my phone to connect to. So I troubleshooted by testing another code from Google AI and that code was successful as well as being able to conenct to. I connected to the access point on my phone.
