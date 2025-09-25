# คำถามประเมินการเขียนโปรแกรม R

กลุ่ม 1 2 3 = q1_dataset:q1_plant_photosynthesis_data.csv
กลุ่ม 4 5 6 = q2_dataset:q2_animal_behavior_data.csv
กลุ่ม 7 8 9 = q3_dataset:q3_microbial_growth_data.csv
กลุ่ม 10 11 12 = q4_dataset:q4_seed_germination_data.csv

สัดส่วนคะแนน
ข้อ 1-4 ข้อละ 1%
ข้อที่ 5 ข้อละ 2%

## Dataset 1: คำถามการทดลองการสังเคราะห์แสงของพืช

**คำอธิบาย Dataset:** พืช 60 ต้นจากสามสายพันธุ์ (Arabidopsis, Tobacco, Spinach) พร้อมการวัดระดับ chlorophyll อัตรา photosynthesis และสภาพแวดล้อม

### คำถาม 1.1 - การสำรวจข้อมูล (Data Exploration)
โหลด plant photosynthesis dataset และใช้ฟังก์ชัน R ที่เหมาะสมเพื่อแสดงแถวแรก 8 แถว ตรวจสอบโครงสร้างของ data frame และสร้าง summary statistics สำหรับตัวแปรทั้งหมด ประเภทข้อมูล (data types) ที่มีอยู่ในแต่ละ column คืออะไร?

### คำถาม 1.2 - การดำเนินการ Vector และ Statistics
แยกการวัด photosynthesis rate ออกมาเป็น vector แยกต่างหาก คำนวณค่าเฉลี่ย (mean) ค่ามัธยฐาน (median) ค่าเบี่ยงเบนมาตรฐาน (standard deviation) ค่าต่ำสุด ค่าสูงสุด และจำนวนการสังเกตทั้งหมด พืชต้นใดที่มี photosynthesis rate สูงสุด?

### คำถาม 1.3 - การวิเคราะห์ข้อมูลเชิงหมวดหมู่ (Categorical Data Analysis)
แปลงตัวแปร Light_Intensity เป็น factor และกำหนดจำนวนพืชที่ทดสอบภายใต้แต่ละสภาวะแสง สร้าง frequency table ที่แสดงการกระจายตัวของพืชในระดับความเข้มแสงต่างๆ

### คำถาม 1.4 - การกรองข้อมูลด้วย Base R (Data Filtering with Base R)
โดยใช้วิธี indexing ของ base R สร้าง subset ที่ประกอบด้วยพืช Arabidopsis เท่านั้นที่มี photosynthesis rates มากกว่า 15.0 มีพืชจำนวนกี่ต้นที่ตรงตามเกณฑ์นี้ และค่าเฉลี่ยของ initial และ final chlorophyll levels คือเท่าไร?

### คำถาม 1.5 - การจัดการข้อมูลด้วย dplyr (Data Manipulation with dplyr)
ใช้ฟังก์ชัน dplyr กรอง dataset ให้รวมเฉพาะพืชที่ปลูกภายใต้สภาวะแสงเข้มสูง (High light intensity) เลือก columns สำหรับ Species, CO2_Level และ Photosynthesis_Rate และจัดเรียงผลลัพธ์ตาม photosynthesis rate จากสูงไปต่ำ

---

## Dataset 2: คำถามการศึกษาพฤติกรรมสัตว์

**คำอธิบาย Dataset:** สัตว์ 75 ตัวจากสามสายพันธุ์ (Rat, Mouse, Hamster) ที่มีการรักษาทางอาหารต่างกันและการวัดพฤติกรรม

### คำถาม 2.1 - การตรวจสอบโครงสร้างข้อมูล (Data Structure Examination)
โหลด animal behavioral dataset และตรวจสอบโครงสร้างโดยใช้ฟังก์ชัน str(), head() และ summary() ระบุตัวแปรใดที่เป็น numeric ตัวแปรใดที่เป็น categorical และกำหนดจำนวนการสังเกตทั้งหมดต่อสายพันธุ์

### คำถาม 2.2 - การวิเคราะห์การเพิ่มน้ำหนัก (Weight Gain Analysis)
คำนวณการเพิ่มน้ำหนักสำหรับสัตว์แต่ละตัวและเพิ่มเป็น column ใหม่ใน data frame กำหนดว่าสัตว์ตัวใดที่มีการเพิ่มน้ำหนักสูงสุดและให้ข้อมูลครบถ้วนรวมถึงสายพันธุ์และประเภทอาหาร

### คำถาม 2.3 - การแปลง Factor และการวิเคราะห์
แปลงตัวแปร Diet_Type เป็น factor และสร้าง frequency table ที่แสดงจำนวนสัตว์ที่ได้รับการรักษาทางอาหารแต่ละประเภท ประเภทอาหารใดที่ใช้บ่อยที่สุดในการศึกษานี้?

### คำถาม 2.4 - การกรองตามอายุ (Age-Based Filtering)
โดยใช้วิธีการของ base R สร้าง subset ที่ประกอบด้วยสัตว์ที่มีอายุระหว่าง 90 ถึง 150 วันเท่านั้น คำนวณค่าเฉลี่ยของ initial weight, final weight และ activity score สำหรับกลุ่มอายุนี้

### คำถาม 2.5 - การเปรียบเทียบสายพันธุ์ด้วย dplyr (Species Comparison with dplyr)
ใช้ฟังก์ชัน dplyr จัดกลุ่มข้อมูลตาม Species และคำนวณค่าเฉลี่ย initial weight, mean final weight และ mean activity score สำหรับแต่ละสายพันธุ์ สายพันธุ์ใดที่มี average activity score สูงสุด?

---

## Dataset 3: คำถามการทดลองการเจริญเติบโตของจุลินทรีย์

**คำอธิบาย Dataset:** เชื้อแบคทีเรีย 48 culture จากสี่สายพันธุ์พร้อมการรักษาด้วย antibiotic และการวัดการเจริญเติบโต

### คำถาม 3.1 - ภาพรวม Dataset
โหลด microbial growth dataset และให้ภาพรวมที่ครอบคลุมรวมถึงจำนวนการสังเกต ประเภทตัวแปร และ summary statistics มี bacterial strains กี่ชนิดที่ทดสอบในการทดลองนี้?

### คำถาม 3.2 - การตรวจสอบการคำนวณ Growth Rate
ตรวจสอบการคำนวณ growth rates โดยการคำนวณ growth rates ด้วยตนเองสำหรับ cultures ห้าตัวแรกโดยใช้สูตร: (Final_OD600 - Initial_OD600) / Growth_Time_Hours การคำนวณของคุณตรงกับค่า Growth_Rate ที่ให้มาหรือไม่?

### คำถาม 3.3 - การวิเคราะห์การรักษาด้วย Antibiotic
สร้าง frequency table ที่แสดงการกระจายตัวของ cultures ในการรักษาด้วย antibiotic ต่างๆ แปลงตัวแปร Antibiotic เป็น factor และกำหนดว่าการรักษาใดที่ใช้บ่อยที่สุด

### คำถาม 3.4 - การสืบสวนผลกระทบของอุณหภูมิ (Temperature Effect Investigation)
กรอง dataset ให้รวมเฉพาะ cultures ที่ปลูกที่อุณหภูมิ 37°C (อุณหภูมิร่างกายมนุษย์ทั่วไป) คำนวณ summary statistics สำหรับ growth rates ที่อุณหภูมินี้และระบุว่า bacterial strain ใดที่มีประสิทธิภาพดีที่สุดภายใต้สภาวะเหล่านี้

### คำถาม 3.5 - การวิเคราะห์เฉพาะ Strain ด้วย dplyr
ใช้ dplyr จัดกลุ่มข้อมูลตาม Bacterial_Strain และคำนวณค่าเฉลี่ย Initial_OD600, Final_OD600 และ Growth_Rate สำหรับแต่ละ strain จัดเรียงผลลัพธ์ตาม average growth rate จากสูงไปต่ำ

---

## Dataset 4: คำถามการศึกษาการงอกของเมล็ดพันธุ์

**คำอธิบาย Dataset:** กลุ่มทดลอง 90 กลุ่มที่ศึกษาการงอกของเมล็ดพันธุ์ในสามสายพันธุ์พืชภายใต้สภาวะดินและการรดน้ำที่แตกต่างกัน

### คำถาม 4.1 - ภาพรวมการออกแบบการทดลอง (Experimental Design Overview)
โหลด seed germination dataset และวิเคราะห์การออกแบบการทดลอง ใช้ฟังก์ชัน R ที่เหมาะสมเพื่อกำหนดจำนวน replicates ที่ใช้สำหรับแต่ละการผสมผสานของ Plant_Species, Soil_Type และ Water_Frequency

### คำถาม 4.2 - การวิเคราะห์ความสำเร็จในการงอก (Germination Success Analysis)
คำนวณ summary statistics สำหรับตัวแปร Seeds_Germinated และ Germination_Percent กลุ่มทดลองใดที่ได้จำนวนเมล็ดงอกสูงสุด และสภาวะสำหรับกลุ่มนี้คืออะไร?

### คำถาม 4.3 - การวิเคราะห์ Factor ประเภทดิน (Soil Type Factor Analysis)
แปลง Soil_Type เป็น factor และสร้างตารางที่แสดงการกระจายตัวของกลุ่มทดลองในประเภทดินต่างๆ คำนวณเปอร์เซ็นต์การงอกเฉลี่ยสำหรับแต่ละประเภทดิน

### คำถาม 4.4 - ประสิทธิภาพเฉพาะสายพันธุ์ (Species-Specific Performance)
กรอง dataset ให้รวมเฉพาะพืช Tomato และคำนวณค่าเฉลี่ย germination percentage, mean days to germination และ mean germination rate สำหรับสายพันธุ์นี้ในทุกสภาวะการทดลอง

### คำถาม 4.5 - ผลกระทบของความถี่การรดน้ำด้วย dplyr (Water Frequency Impact with dplyr)
ใช้ฟังก์ชัน dplyr จัดกลุ่มข้อมูลตาม Water_Frequency และคำนวณค่าเฉลี่ย germination percentage และ average days to germination สำหรับแต่ละตารางการรดน้ำ ความถี่การรดน้ำใดที่ให้ผลการงอกดีที่สุด?

---