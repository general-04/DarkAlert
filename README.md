# DarkAlert 🔔

<div align="center">
  
![DarkAlert Banner]()

**DarkAlertv2**

[![Version](https://img.shields.io/badge/version-2.0.0-8B5CF6.svg)](https://github.com/yourusername/darkalert)
[![Size](https://img.shields.io/badge/size-6.7kb-4F46E5.svg)]()

</div>

## ✨ คุณสมบัติ

- 🌑 ธีมดาร์กโหมดที่ออกแบบมาแบบเดียว
- 📱 Responsive Design
- 🛠️ Flexible customization  

## 📦 การติดตั้ง

### วิธีที่ 1: ผ่าน CDN

```html
<link href="https://cdn.example.com/darkalertv2.min.css" rel="stylesheet">
<script src="https://cdn.example.com/darkalertv2.min.js"></script>
```

### วิธีที่ 2: ดาวน์โหลดโดยตรง

[ดาวน์โหลด DarkAlert v2.0.0](https://github.com/yourusername/darkalert/releases/latest)

## 🚀 การใช้งานเบื้องต้น

```javascript
// แจ้งเตือนพื้นฐาน
DarkAlert.fire({
    title: 'การแจ้งเตือนพื้นฐาน',
    text: 'สวัสดี!'
});

// แจ้งเตือนสำเร็จ
DarkAlert.success({
    title: 'สำเร็จ!',
    text: 'ดำเนินการเสร็จสิ้น'
});

// แจ้งเตือนผิดพลาด
DarkAlert.error({
    title: 'ผิดพลาด!',
    text: 'เกิดข้อผิดพลาดบางอย่าง'
});

// Toast การแจ้งเตือน
DarkAlert.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย'
});
```

## ⚙️ การกำหนดค่า

```javascript
DarkAlert.fire({
    title: '',                 // หัวข้อ
    text: '',                  // ข้อความ
    icon: 'info',              // ไอคอน (info, success, error, warning)
    showConfirmButton: true,   // แสดงปุ่มยืนยัน
    showCancelButton: false,   // แสดงปุ่มยกเลิก
    confirmButtonText: 'OK',   // ข้อความปุ่มยืนยัน
    cancelButtonText: 'Cancel',// ข้อความปุ่มยกเลิก
    confirmCallback: null,     // ฟังก์ชันเมื่อคลิกปุ่มยืนยัน
    cancelCallback: null,      // ฟังก์ชันเมื่อคลิกปุ่มยกเลิก
    closeOnOverlayClick: true, // ปิดเมื่อคลิกภายนอก
    progress: false,           // แสดงแถบโหลด
    timer: null,               // ตั้งเวลาปิดอัตโนมัติ (มิลลิวินาที)
    position: 'center',        // ตำแหน่ง (center, top, bottom)
    animation: true,           // เปิด/ปิดการเคลื่อนไหว
    customClass: '',           // คลาสเพิ่มเติม
    allowOutsideClick: true,   // อนุญาตให้คลิกภายนอกเพื่อปิด
    backdrop: true,            // แสดงพื้นหลังทึบ
    toast: false,              // โหมด Toast
    toastPosition: 'bottom-end'// ตำแหน่ง Toast
});
```

## 🎭 ประเภทการแจ้งเตือน

DarkAlert มาพร้อมกับประเภทการแจ้งเตือนสำเร็จรูปหลายแบบ:

### การแจ้งเตือนพื้นฐาน

```javascript
DarkAlert.fire({
    title: 'การแจ้งเตือนพื้นฐาน',
    text: 'สวัสดี!'
});
```

### การแจ้งเตือนสำเร็จ

```javascript
DarkAlert.success({
    title: 'สำเร็จ!',
    text: 'ดำเนินการเสร็จสิ้น'
});
```

### การแจ้งเตือนข้อผิดพลาด

```javascript
DarkAlert.error({
    title: 'ผิดพลาด!',
    text: 'เกิดข้อผิดพลาดบางอย่าง'
});
```

### การแจ้งเตือนคำเตือน

```javascript
DarkAlert.warning({
    title: 'คำเตือน!',
    text: 'โปรดระมัดระวัง'
});
```

### การแจ้งเตือนข้อมูล

```javascript
DarkAlert.info({
    title: 'ข้อมูล',
    text: 'นี่คือข้อมูลสำคัญ'
});
```

## 🍞 การใช้งานโหมด Toast

Toast เป็นการแจ้งเตือนแบบชั่วคราวที่ปรากฏที่มุมหน้าจอ:

```javascript
// Toast สำเร็จ
DarkAlert.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย'
});

// Toast ผิดพลาด
DarkAlert.errorToast({
    text: 'ไม่สามารถบันทึกข้อมูลได้'
});

// Toast คำเตือน
DarkAlert.warningToast({
    text: 'การเชื่อมต่อไม่เสถียร'
});

// กำหนดตำแหน่ง Toast
DarkAlert.successToast({
    text: 'บันทึกข้อมูลเรียบร้อย',
    toastPosition: 'top-end' // top, top-start, top-end, bottom, bottom-start, bottom-end
});
```

## 🌟 คุณสมบัติขั้นสูง

### การยืนยันการทำรายการ

```javascript
DarkAlert.fire({
    title: 'ยืนยันการทำรายการ',
    text: 'คุณต้องการดำเนินการต่อหรือไม่?',
    showCancelButton: true,
    confirmButtonText: 'ยืนยัน',
    cancelButtonText: 'ยกเลิก',
    confirmCallback: () => {
        console.log('ผู้ใช้ยืนยันการทำรายการ');
    },
    cancelCallback: () => {
        console.log('ผู้ใช้ยกเลิกการทำรายการ');
    }
});
```

### การปิดอัตโนมัติ

```javascript
DarkAlert.fire({
    title: 'ปิดอัตโนมัติ',
    text: 'จะปิดใน 2 วินาที',
    timer: 2000
});
```

### สถานะกำลังโหลด

```javascript
DarkAlert.loading({
    title: 'กำลังโหลด',
    text: 'กรุณารอสักครู่...'
});

// ปิดการแจ้งเตือนกำลังโหลด
setTimeout(() => {
    DarkAlert.close();
}, 3000);
```
