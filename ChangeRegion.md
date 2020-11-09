# Galaxy Watch Active 2

## Change Region

### สำรองข้อมูล Galaxy Watch

Galaxy Wearable แท็ป **Settings** ไปที่ **About watch > Backup and restore > Backup settings >** กดปุ่ม **Back up now**

### เปิด Developer Mode, Debugging และเชื่อมต่อ Wi-Fi

บนนาฬิกา ไปที่ **Settings > About watch > Software** จากนั้นแตะที่ **Software version 7 ครั้ง** จนขึ้นว่า Developer mode turned on

**กด Back** กลับไปหน้า About watch เลื่อนไปด้านล่าง กดเปิด Debugging กดเปิดแล้ว **กด OK** ปิดนาฬิกาแล้วเปิดใหม่

เชื่อมต่อ WiFi ไปที่ **Settings > Connections > Bluetooth** เลื่อน **ปิด Bluetooth** กด back

กลับไปหน้า Connections เลื่อนไปที่ **Wi-Fi > Wi-Fi networks แล้ว connect Wi-Fi** เมื่อเชื่อมต่อแล้ว แตะที่ชื่อ Wi-Fi เลื่อนไปข้างล่างสุดตรง IP address จดหมายเลข IP address ไว้

### ใช้ sdb เชื่อมต่อนาฬิกา

เข้าไปที่โฟเดอร์ **sdb*2.2.60*\<OS\>\data\tools** ดับเบิ้ลคลิกที่ sdb จะมีหน้าต่าง terminal เปิดขึ้นมา

พิมพ์ sdb connect (เว้นวรรค) หมายเลข IP address ที่จดไว้ตะกี้

```bash
sdb connect 192.168.1.86
```

นาฬิกาจะขึ้นให้กดอนุญาต **กด OK**

บนหน้าต่าง **terminal** จะขึ้น failed to connect แต่ถ้าพิมพ์คำสั่งเดิมไป จะขึ้นว่า **already connected** แล้ว

### เรียกหน้าต่างเลือก Region <ไม่รองรับ>

```bash
sdb shell
```

กด enter จะขึ้น **sh-3.2\$** จากนั้นพิมพ์

```bash
launch_app csc-manager.csc-pre-configuration
```

ที่นาฬิกาจะขึ้น **CSC Pre-config** จากนั้นเลื่อนไปบนสุดเลือก **XAR**
จากนั้นนาฬิกาจะรีเซ็ตตัวเอง

เชื่อมต่อ VPN ไปยัง US ที่โทรศัพท์ แล้วเชื่อมต่อ Galaxy Watch กับมือถือและติดตั้ง Samsung Pay ที่มือถือ ไปที่ **Bluetooth Settings** จากนั้นกด **Unpair** นาฬิกา Galaxy Watch

ไปที่ App Settings ของ Galaxy Wearable กดที่ **Storage** จากนั้นกด **Clear Data**

เปิด Galaxy Wearable แล้วเชื่อมต่อนาฬิกาตามปกติ ที่หน้า Restore **เลือก Restore** ข้อมูลกลับมา# Galaxy Watch Active 2 - Samsung Pay & Blood Pressure & ECG

### Question

Question: เปลี่ยน region กลับเป็นไทย=?

Answer: เปลี่ยน XAR เป็น THO แทน
