# ✦ SketchPro 3D — Professional Drawing & 3D Tool

โปรแกรมวาดภาพ 2D/3D แบบ SketchUp-style สำหรับ Browser พร้อมระบบ AI แปลงภาพ 2D เป็น 3D

![SketchPro 3D](https://img.shields.io/badge/version-4.0-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![HTML](https://img.shields.io/badge/tech-HTML%2FCSS%2FJS-orange)

---

## 🚀 ติดตั้งและใช้งาน

### วิธีที่ 1 — เปิดไฟล์โดยตรง (ง่ายที่สุด)
```bash
# Clone repo
git clone https://github.com/YOUR_USERNAME/sketchpro3d.git
cd sketchpro3d

# เปิดไฟล์ใน browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### วิธีที่ 2 — รันด้วย Local Server (แนะนำ สำหรับ AI features)
```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve .

# หลังจากนั้นเปิด http://localhost:8000
```

### วิธีที่ 3 — GitHub Pages (Host ฟรี)
1. Push โค้ดขึ้น GitHub
2. ไปที่ Settings → Pages
3. เลือก Branch: main, Folder: / (root)
4. บันทึก — ได้ URL `https://username.github.io/sketchpro3d`

---

## ✨ ฟีเจอร์หลัก

### 🎨 วาดภาพ 2D
| เครื่องมือ | คีย์ลัด | คำอธิบาย |
|-----------|---------|---------|
| ดินสอ | P | วาดเส้นอิสระ |
| แปรง | B | วาดด้วย soft brush |
| ยางลบ | E | ลบเส้น |
| เติมสี | F | Flood fill สี |
| หยิบสี | I | Eyedropper |
| เส้นตรง | L | วาดเส้นตรง |
| สี่เหลี่ยม | R | วาดสี่เหลี่ยม |
| วงกลม | C | วาดวงกลม/วงรี |
| ข้อความ | T | เพิ่มข้อความ |
| สเปรย์ | — | Spray paint |

### 🧊 เครื่องมือ 3D (SketchUp-style)
| เครื่องมือ | คำอธิบาย |
|-----------|---------|
| **Box3D** | วาดกล่อง 3D แบบ Isometric ลากได้ทันที |
| **Push/Pull** | คลิกเพื่อยกวัตถุในพื้นที่ 3D |
| **Iso Line** | วาดเส้นบน Isometric grid (snap อัตโนมัติ) |
| **Ruler** | วัดระยะจริงด้วยหน่วยที่เลือก |

### 📏 ระบบวัดขนาด
- วัดระยะ, มุม, dx, dy ในหน่วยจริง
- รองรับ: เมตร, เซนติเมตร, มิลลิเมตร, ฟุต, นิ้ว, พิกเซล
- ตั้งค่า Scale (px ต่อหน่วย) ได้

### 🤖 AI 2D → 3D
- ส่งภาพที่วาดหรือรูปที่นำเข้าให้ Claude AI วิเคราะห์
- สไตล์: Realistic, Cartoon, Wireframe, Clay, Isometric, Toon
- ปรับ: ความลึก, แสง, มุมมอง, เงา
- ต้องการ Anthropic API key (ดู Configuration)

### 📱 รองรับแท็บเล็ต
- Touch events ครบ (ลาก, วาด, แพน)
- Pinch-to-zoom ด้วยสองนิ้ว
- ปุ่มขนาดใหญ่เหมาะกับนิ้ว

---

## ⚙️ Configuration (สำหรับ AI Features)

ฟีเจอร์ AI ต้องการ Anthropic API key  
เปิดไฟล์ `index.html` ค้นหา `fetch('https://api.anthropic.com/v1/messages'`  
ใส่ header `'x-api-key': 'YOUR_KEY'` หรือใช้ proxy server

> **หมายเหตุ**: API key ไม่ควรอยู่ใน frontend code สาธารณะ  
> แนะนำให้ใช้ backend proxy สำหรับ production

---

## 🗂️ โครงสร้างไฟล์

```
sketchpro3d/
├── index.html          # แอปหลัก (ไฟล์เดียว, ไม่ต้องติดตั้งอะไร)
├── README.md           # คู่มือนี้
└── LICENSE             # MIT License
```

---

## ⌨️ Keyboard Shortcuts

| คีย์ | การทำงาน |
|-----|---------|
| P | ดินสอ |
| B | แปรง |
| E | ยางลบ |
| R | สี่เหลี่ยม |
| C | วงกลม |
| L | เส้นตรง |
| T | ข้อความ |
| F | เติมสี |
| I | หยิบสี |
| H | แพน |
| Z | ซูม |
| M | วัดระยะ |
| + / - | ซูมเข้า/ออก |
| 0 | รีเซ็ตมุมมอง |
| Ctrl+Z | เลิกทำ |
| Ctrl+Y | ทำซ้ำ |
| Ctrl+S | บันทึก PNG |
| Esc | ยกเลิก |

---

## 🖱️ Mouse / Touch

| การกระทำ | ผล |
|---------|---|
| Scroll wheel | ซูมเข้า/ออก |
| Middle click drag | แพน |
| H + drag | แพน |
| Pinch (touch) | ซูม |
| Drag & Drop ไฟล์ | นำเข้ารูป |
| Ctrl+V | วางรูปจาก Clipboard |

---

## 📝 License

MIT License — ใช้งานได้ฟรี แก้ไขได้ แจกจ่ายได้

---

## 🙏 Credits

Built with vanilla HTML/CSS/JS + Anthropic Claude API  
SketchPro 3D Professional v4.0
