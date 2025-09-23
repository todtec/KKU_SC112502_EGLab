# R, RStudio, and dplyr Installation Guide

## English Version

### Installing R Programming Language

R is a free software environment for statistical computing and graphics. Follow these steps to install R on your system.

#### Step 1: Download R
Visit the official R download page: **https://cran.r-project.org/**

1. Click on "Download R for Windows" (or your operating system)
2. Click on "base" 
3. Click on "Download R-4.x.x for Windows" (latest version)
4. Save the installer file to your computer

#### Step 2: Install R
1. Run the downloaded installer file
2. Follow the installation wizard prompts
3. Accept the default settings unless you have specific requirements
4. Click "Finish" when installation is complete

### Installing RStudio

RStudio is an integrated development environment (IDE) for R that provides enhanced functionality and user interface.

#### Step 1: Download RStudio
Visit the official RStudio download page: **https://posit.co/downloads/**

1. Scroll down to "RStudio Desktop"
2. Click "Download RStudio Desktop"
3. The website will automatically detect your operating system
4. Click the download button for the recommended version
5. Save the installer file to your computer

#### Step 2: Install RStudio
1. Run the downloaded RStudio installer
2. Follow the installation prompts
3. Accept the license agreement
4. Choose installation directory (default is recommended)
5. Click "Install" and then "Finish"

### Installing dplyr Package

The dplyr package provides a grammar of data manipulation with fast, consistent tools for common data manipulation tasks.

#### Method 1: Using RStudio Console
1. Open RStudio
2. In the Console pane, type the following command:
   ```r
   install.packages("dplyr")
   ```
3. Press Enter and wait for the installation to complete
4. Load the package using:
   ```r
   library(dplyr)
   ```

#### Method 2: Using RStudio Package Manager
1. Open RStudio
2. Navigate to the "Packages" tab in the bottom-right pane
3. Click "Install"
4. Type "dplyr" in the Packages field
5. Click "Install"

### Verification
To verify successful installation, run the following commands in RStudio:
```r
# Check R version
R.version.string

# Check if dplyr is installed and load it
library(dplyr)

# Test dplyr functionality
data(mtcars)
mtcars %>% filter(mpg > 20) %>% head()
```

---

## Thai Version (เวอร์ชันภาษาไทย)

### การติดตั้ง R Programming Language

R เป็นซอฟต์แวร์ฟรีสำหรับการคำนวณทางสถิติและการสร้างกราฟ ทำตามขั้นตอนเหล่านี้เพื่อติดตั้ง R ในระบบของคุณ

#### ขั้นตอนที่ 1: ดาวน์โหลด R
เข้าไปที่หน้าดาวน์โหลด R อย่างเป็นทางการ: **https://cran.r-project.org/**

1. คลิกที่ "Download R for Windows" (หรือระบบปฏิบัติการของคุณ)
2. คลิกที่ "base"
3. คลิกที่ "Download R-4.x.x for Windows" (เวอร์ชันล่าสุด)
4. บันทึกไฟล์ติดตั้งลงในคอมพิวเตอร์ของคุณ

#### ขั้นตอนที่ 2: ติดตั้ง R
1. เรียกใช้ไฟล์ติดตั้งที่ดาวน์โหลดมา
2. ทำตามคำแนะนำของตัวช่วยติดตั้ง
3. ยอมรับการตั้งค่าเริ่มต้น เว้นแต่คุณจะมีข้อกำหนดเฉพาะ
4. คลิก "Finish" เมื่อการติดตั้งเสร็จสมบูรณ์

### การติดตั้ง RStudio

RStudio เป็นสภาพแวดล้อมการพัฒนาแบบรวม (IDE) สำหรับ R ที่ให้ฟังก์ชันและส่วนติดต่อผู้ใช้ที่ปรับปรุงแล้ว

#### ขั้นตอนที่ 1: ดาวน์โหลด RStudio
เข้าไปที่หน้าดาวน์โหลด RStudio อย่างเป็นทางการ: **https://posit.co/downloads/**

1. เลื่อนลงไปที่ "RStudio Desktop"
2. คลิก "Download RStudio Desktop"
3. เว็บไซต์จะตรวจจับระบบปฏิบัติการของคุณโดยอัตโนมัติ
4. คลิกปุ่มดาวน์โหลดสำหรับเวอร์ชันที่แนะนำ
5. บันทึกไฟล์ติดตั้งลงในคอมพิวเตอร์ของคุณ

#### ขั้นตอนที่ 2: ติดตั้ง RStudio
1. เรียกใช้ไฟล์ติดตั้ง RStudio ที่ดาวน์โหลดมา
2. ทำตามคำแนะนำการติดตั้ง
3. ยอมรับข้อตกลงใบอนุญาต
4. เลือกไดเร็กทอรีการติดตั้ง (แนะนำให้ใช้ค่าเริ่มต้น)
5. คลิก "Install" แล้วคลิก "Finish"

### การติดตั้งแพ็กเกจ dplyr

แพ็กเกจ dplyr ให้ไวยากรณ์การจัดการข้อมูลพร้อมเครื่องมือที่รวดเร็วและสม่ำเสมอสำหรับงานการจัดการข้อมูลทั่วไป

#### วิธีที่ 1: ใช้ RStudio Console
1. เปิด RStudio
2. ในหน้าต่าง Console พิมพ์คำสั่งต่อไปนี้:
   ```r
   install.packages("dplyr")
   ```
3. กด Enter และรอให้การติดตั้งเสร็จสมบูรณ์
4. โหลดแพ็กเกจโดยใช้:
   ```r
   library(dplyr)
   ```

#### วิธีที่ 2: ใช้ RStudio Package Manager
1. เปิด RStudio
2. ไปที่แท็บ "Packages" ในหน้าต่างด้านล่างขวา
3. คลิก "Install"
4. พิมพ์ "dplyr" ในช่อง Packages
5. คลิก "Install"

### การตรวจสอบ
เพื่อตรวจสอบการติดตั้งที่สำเร็จ ให้รันคำสั่งต่อไปนี้ใน RStudio:
```r
# ตรวจสอบเวอร์ชัน R
R.version.string

# ตรวจสอบว่า dplyr ติดตั้งแล้วและโหลดมัน
library(dplyr)

# ทดสอบฟังก์ชัน dplyr
data(mtcars)
mtcars %>% filter(mpg > 20) %>% head()
```

## Additional Notes / หมายเหตุเพิ่มเติม

**System Requirements / ความต้องการของระบบ:**
- Windows 10/11, macOS 10.15+, or Linux
- At least 2GB RAM / RAM อย่างน้อย 2GB
- 500MB free disk space / พื้นที่ว่างในดิสก์ 500MB

**Troubleshooting / แก้ไขปัญหา:**
- If installation fails, run as administrator / หากการติดตั้งล้มเหลว ให้รันในฐานะผู้ดูแลระบบ
- Ensure internet connection for package installation / ตรวจสอบการเชื่อมต่ออินเทอร์เน็ตสำหรับการติดตั้งแพ็กเกจ
- Update R and RStudio regularly / อัปเดต R และ RStudio เป็นประจำ