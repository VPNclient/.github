# VPN Client

[🇬🇧 English](README.md) | [🇷🇺 Russian](README_ru.md) | [🇹🇭 ไทย](README_th.md)

---

**VPN Client** เป็นไคลเอนต์ VPN แบบข้ามแพลตฟอร์มที่รองรับหลายแกนและหลายโปรโตคอล

## คุณสมบัติเด่น

- **รองรับหลายโปรโตคอล**: Xray (VMess, VLESS, Reality, Shadowsocks, Trojan, SSH), OpenVPN, WireGuard รวมถึง SOCKS5/HTTP/HTTPS proxy
- **ข้ามแพลตฟอร์ม**: ใช้งานได้กับ iOS, Android, macOS, Windows และ Linux
- **ประสิทธิภาพสูง**: ฟังก์ชันหลักพัฒนาเป็น native ด้วย Swift (สำหรับ iOS) และ Kotlin (สำหรับ Android) พร้อมการประมวลผลที่สำคัญด้วย C++ และ Golang เพื่อความเร็วและความเสถียร

## สถาปัตยกรรมระบบ

ระบบ VPN Client แบ่งออกเป็นหลายระดับ:

1. **VPNclient-engine**  
   แกนหลักของแต่ละแพลตฟอร์ม ทำหน้าที่จัดการการเชื่อมต่อ VPN, การกำหนดเส้นทางทราฟฟิก, การเชื่อมต่อกับระบบปฏิบัติการ และการสื่อสารกับโปรโตคอล VPN ต่าง ๆ เช่น OpenVPN, WireGuard, Xray เป็นต้น

2. **ตัวเชื่อมแต่ละแพลตฟอร์ม:**
   - **[VPNclient-engine-flutter](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     ปลั๊กอินสำหรับ Flutter โดยใช้ `MethodChannel` ในการสื่อสารกับโค้ด native
   - **[VPNclient-engine-react-native](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     ตัวเชื่อมสำหรับ React Native โดยใช้ `NativeModules`

3. **VPN Client App**  
   แอปที่พัฒนาด้วย Flutter ใช้ปลั๊กอินข้างต้นในการจัดการการเชื่อมต่อ VPN และแสดงสถานะ

![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme2.png)

## รองรับแพลตฟอร์ม

- iOS
- Android
- macOS
- Windows
- Linux

## ที่เก็บซอร์สโค้ด

- [VPNclient-app](https://github.com/VPNclient/VPNclient-app) – แอปตัวอย่างที่สร้างด้วย Flutter  
- [VPNclient-engine-flutter](https://github.com/VPNclient/VPNclient-engine-flutter) – แกน VPN สำหรับ Flutter  
- [VPNclient-engine-android](https://github.com/VPNclient/VPNclient-engine-android) – แกน VPN สำหรับ Android  
- [VPNclient-engine-ios](https://github.com/VPNclient/VPNclient-engine-ios) – แกน VPN สำหรับ iOS  
- [VPNclient-engine-windows](https://github.com/VPNclient/VPNclient-engine-windows) – แกน VPN สำหรับ Windows  
- [VPNclient-engine-linux](https://github.com/VPNclient/VPNclient-engine-linux) – แกน VPN สำหรับ Linux  

## แอปตัวอย่าง

- [SuperHit-VPNclient-app](https://github.com/VPNclient/SuperHit-VPNclient-app)
- [fineVPN-VPNclient-app](https://github.com/VPNclient/fineVPN-VPNclient-app)

## ข้อดีของ VPN Client Engine

1. การเชื่อมต่อกับระบบปฏิบัติการอย่างเป็น native  
2. ความยืดหยุ่นในการใช้งานและปรับแต่ง  
3. โค้ดแบบโอเพ่นซอร์ส

## วิธีเริ่มต้นใช้งาน

เลือกที่เก็บซอร์สโค้ดตามแพลตฟอร์มที่คุณใช้ แล้วทำตามคำแนะนำใน README ของที่เก็บนั้น

## ใบอนุญาต

โปรเจกต์นี้อยู่ภายใต้ Extended GPLv3 ดูรายละเอียดเพิ่มเติมได้ในไฟล์ [LICENSE](LICENSE.md)

## ติดต่อ

เว็บไซต์: [vpnclient.click](https://vpnclient.click/)
