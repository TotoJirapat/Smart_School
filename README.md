🏫 Smart School
ระบบจัดการข้อมูลโรงเรียน (Smart School) เป็นโครงงานสำหรับพัฒนาระบบสารสนเทศเพื่อช่วยจัดการข้อมูลภายในโรงเรียน โดยมีการแบ่งการทำงานออกเป็น Frontend Application, Backend API และ Database เพื่อให้แต่ละส่วนสามารถทำงานร่วมกันอย่างเป็นระบบ
ระบบพัฒนาด้วย Flutter สำหรับส่วนติดต่อผู้ใช้ และ Backend API สำหรับจัดการข้อมูลและเชื่อมต่อกับฐานข้อมูล

👨‍💻 Developer

JIRAPAT KAEWKRAJANG 6620310131
NIIRFAN POHMAE 6620310008
# 🔎 Source Code สำหรับตรวจสอบ

สำหรับการตรวจสอบ Source Code ของระบบ **Smart School** สามารถตรวจสอบได้จาก 2 ส่วนหลัก ดังนี้

---

## 1. ⚙️ Backend API

สามารถตรวจสอบ Source Code ของ Backend ได้ที่โฟลเดอร์

**`backend/api`**

👉 [เปิด Backend API](https://github.com/TotoJirapat/Smart_School/tree/main/backend/api)

ภายในส่วนนี้เป็น Source Code ที่ทำหน้าที่เป็น **Backend API** ของระบบ โดยทำหน้าที่เป็นตัวกลางระหว่าง Flutter Application และ Database

### หน้าที่หลักของ Backend API

* รับ Request จาก Flutter Application
* ประมวลผลข้อมูล
* ติดต่อและจัดการข้อมูลใน Database
* ดำเนินการ CRUD ได้แก่

  * Create
  * Read
  * Update
  * Delete
* ส่งข้อมูลกลับไปยัง Flutter Application
* จัดการ API และ Logic ที่เกี่ยวข้องกับระบบ

### Flow การทำงานโดยสรุป

```text
Flutter Application
        │
        │ HTTP Request
        ▼
   Backend API
        │
        │ Query
        ▼
     Database
        │
        │ Result
        ▼
   Backend API
        │
        │ JSON Response
        ▼
Flutter Application
```

---

## 2. 📱 Flutter Application

สามารถตรวจสอบ Source Code ของ Flutter Application ได้ที่

**`flutter_application_1/lib`**

👉 [เปิด Flutter Application / lib](https://github.com/Niirfan/Smart_School/tree/main/flutter_application_1/lib)

โดยให้ตรวจสอบ **ไฟล์และโฟลเดอร์ทั้งหมดภายใน `lib`**

ส่วน `lib` เป็นส่วนหลักของ Source Code ของ Flutter Application ซึ่งประกอบด้วยโค้ดสำหรับ

* User Interface (UI)
* หน้าต่างต่าง ๆ ของ Application
* Widget
* Navigation
* Model
* การเรียกใช้งาน API
* การรับและส่งข้อมูล
* Logic ของ Application
* การจัดการข้อมูลที่ได้รับจาก Backend

### Flow การทำงานของ Flutter

```text
ผู้ใช้งาน
    │
    ▼
Flutter UI
    │
    │ User Action
    ▼
Application Logic
    │
    │ API Request
    ▼
Backend API
    │
    │ JSON Response
    ▼
Flutter
    │
    ▼
แสดงผลบนหน้าจอ
```

---

## 📌 ขอบเขต Source Code ที่ต้องการให้ตรวจสอบ

| ลำดับ | ส่วนที่ตรวจสอบ      | ตำแหน่ง                     |
| ----- | ------------------- | --------------------------- |
| 1     | Backend API         | `backend/api`               |
| 2     | Flutter Application | `flutter_application_1/lib` |
| 3     | Database            | ไฟล์ `.sql` ใน Repository   |

### 🔗 ลิงก์สำหรับตรวจสอบ

* ⚙️ **Backend API:** [backend/api](https://github.com/TotoJirapat/Smart_School/tree/main/backend/api)
* 📱 **Flutter Source Code:** [flutter_application_1/lib](https://github.com/Niirfan/Smart_School/tree/main/flutter_application_1/lib)
* 🗄️ **Database:** [Smart School SQL Database](https://github.com/TotoJirapat/Smart_School/blob/main/6620310131_smartschool_db%20%285%29.sql)

---

## 👨‍🏫 หมายเหตุสำหรับการตรวจสอบ

> **สำหรับอาจารย์ผู้ตรวจสอบโครงงาน**
>
> สามารถตรวจสอบการพัฒนาระบบจาก Source Code หลักได้ 2 ส่วน ได้แก่
>
> **1. Backend API** ที่ `backend/api`
> ใช้สำหรับตรวจสอบการทำงานของ Server, API และการจัดการข้อมูล
>
> **2. Flutter Application** ที่ `flutter_application_1/lib`
> ใช้สำหรับตรวจสอบส่วน Frontend, User Interface และ Logic ของ Application
>
> ทั้งสองส่วนทำงานร่วมกันผ่าน API เพื่อรับส่งข้อมูลระหว่าง Application และ Backend
