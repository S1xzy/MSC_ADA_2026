# MSc. SC677 701 Advanced Data Analysis

## Description
**Project:**  วิธีการดาวน์โหลด และขั้นตอนการใช้ Virsual Environment (venv) ของ Python และ Github<br>
**Subject:** SC677 701 Advanced Data Analysis การวิเคราะห์ข้อมูลขั้นสูง<br>
**Semester** Second/2026, Department of Statistics, Faculty of Science, Khon Kaen University<br>
**Name:** Supawit Chaingam (Ps)<br>
**Student ID:** 695020003 - 1<br>

**🧑‍💼 Course Lecturer** \
**Asst. Prof. Prem Junsawang**
> **Lecturer at KKU** \
> Faculty of Science, Department of Statistics, Khon Kaen University 

---

## Installation
### 1. Based Python and Github
1. Download and Install Python (v. 3.10 or more over) from [python.org](https://www.python.org/)
2. Download and Install Git from [git-scm.com](https://git-scm.com/)
3. From the 1. and 2. if installation completed, open the Terminal or Command Prompt and check the version of python and git installation.

### 2. Project Cloning (Github)
Copy the repository link from Github and use 
```bash
git clone [https://github.com/](https://github.com/)<username>/MSC_ADA_2026.git
cd MSC_ADA_2026
```

### 3. Create Virtual Environment (venv)
1. Create virtual environment `venv.` in the project's folder
```bash
# Researved for Windows
python -m venv .venv
```

2. Activate venv
```bash
   # Reserved for Windows (PowerShell)
   .venv\Scripts\Activate.ps1

   # Reserved for Windows (Command Prompt)
   .venv\Scripts\activate
```
*when venv activated, the `(.venv)` will show in from of the command line in thhe terminal*

### 4. Libraries
Update `pip` to latest version at first and then install the essential packgaes for the project
*(For this project, the library pandas numpy requests jupyter are installed)*

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

## Essential Commands for `venv` and `pip`
| คำสั่ง (Command) | หน้าที่และการทำงาน |
| :--- | :--- |
| `python -m venv .venv` | สร้างสภาพแวดล้อมเสมือน (Virtual Environment) ชื่อ `.venv` เพื่อแยกไลบรารีของโปรเจกต์นี้ออกจากระบบหลักของเครื่อง (บน macOS/Linux ใช้ `python3`) |
| `.venv\Scripts\Activate.ps1` | เปิดใช้งาน (Activate) สภาพแวดล้อมเสมือนบน Windows PowerShell (หากใช้ Command Prompt ใช้ `.venv\Scripts\activate` และ macOS/Linux ใช้ `source .venv/bin/activate`) |
| `deactivate` | ปิดการใช้งาน (ออกจาก) Virtual Environment ปัจจุบัน เพื่อกลับไปใช้สภาพแวดล้อมหลักของระบบ |
| `pip install <package_name>` | ดาวน์โหลดและติดตั้งไลบรารีหรือแพ็กเกจเสริมของ Python ที่ระบุไว้ลงในสภาพแวดล้อมปัจจุบัน |
| `pip list` | แสดงรายชื่อแพ็กเกจทั้งหมดพร้อมเลขเวอร์ชันที่ถูกติดตั้งอยู่ในสภาพแวดล้อมปัจจุบัน |
| `pip freeze > requirements.txt` | ส่งออกรายชื่อแพ็กเกจทั้งหมดและเวอร์ชันที่ติดตั้งอยู่ บันทึกลงในไฟล์ `requirements.txt` เพื่อใช้ส่งต่อให้ผู้อื่นติดตั้งตามได้เหมือนกัน |
| `pip install -r requirements.txt` | อ่านรายชื่อแพ็กเกจจากไฟล์ `requirements.txt` และติดตั้งไลบรารีทั้งหมดตามเวอร์ชันที่ระบุไว้โดยอัตโนมัติ |

## Essential Commands for Git
| คำสั่ง (Command) | หน้าที่และการทำงาน |
| :--- | :--- |
| `git init` | เริ่มต้นสร้าง Local Git Repository ใหม่ในโฟลเดอร์โปรเจกต์ปัจจุบัน เพื่อให้ Git เริ่มติดตามการเปลี่ยนแปลงของไฟล์ |
| `git status` | ตรวจสอบสถานะของไฟล์ในโปรเจกต์ เช่น ไฟล์ที่ถูกแก้ไข ไฟล์ที่สร้างใหม่ หรือไฟล์ที่ถูกเตรียมพร้อมสำหรับการ Commit (Staging Area) |
| `git add .` | เพิ่มไฟล์ที่มีการเปลี่ยนแปลงทั้งหมดเข้าสู่ Staging Area เพื่อเตรียมความพร้อมก่อนบันทึกการเปลี่ยนแปลง (หากต้องการระบุเฉพาะไฟล์ใช้ `git add <ชื่อไฟล์>`) |
| `git commit -m "..."` | บันทึกการเปลี่ยนแปลงของไฟล์ที่อยู่ใน Staging Area ลงในประวัติของ Local Repository พร้อมแนบข้อความอธิบายการแก้ไขในเครื่องหมายคำพูด |
| `git branch -M main` | เปลี่ยนชื่อ Branch หลักของโปรเจกต์ปัจจุบันให้เป็น `main` เพื่อให้ตรงกับมาตรฐานของ GitHub |
| `git remote add origin <url>` | เชื่อมต่อ Local Repository ในเครื่องเข้ากับ Remote Repository บน GitHub ตามลิงก์ `<url>` ที่ระบุ โดยตั้งชื่อจุดเชื่อมต่อว่า `origin` |
| `git push -u origin main` | อัปโหลด (Push) ประวัติการ Commit ทั้งหมดจาก Branch `main` ในเครื่องขึ้นไปยัง Remote Repository (`origin`) บน GitHub |
| `git pull` | ดึงข้อมูลและอัปเดตการเปลี่ยนแปลงล่าสุดจาก Remote Repository บน GitHub ลงมาผสานเข้ากับโค้ดในเครื่อง |
| `git clone <url>` | คัดลอก (ดาวน์โหลด) โปรเจกต์ทั้งหมด รวมถึงประวัติการแก้ไขจาก Remote Repository ตาม `<url>` ลงมาไว้ในเครื่องคอมพิวเตอร์ |