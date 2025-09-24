# Practice Questions for Biological Datasets
## คำถามฝึกหัดสำหรับชุดข้อมูลทางชีววิทยา

Based on the four biological datasets generated in class, complete the following exercises using R programming techniques learned in the course.

# Group Assignment
Group 1 2 3 = q1_dataset
Group 4 5 6 = q2_dataset
Group 7 8 9 = q3_dataset
Group 10 11 12 = q4_dataset

---

## Dataset 1: Plant Photosynthesis Experiment
## ชุดข้อมูลที่ 1: การทดลองการสังเคราะห์แสงของพืช

**English Version:**

1. Calculate the mean, median, and standard deviation of the Initial_Chlorophyll values for all plants in the dataset. Create a summary table showing these descriptive statistics.

2. Create a histogram of the Photosynthesis_Rate variable with appropriate title and axis labels. Describe what the distribution tells you about the data.

3. Use the filter() function from dplyr to select only plants with High light intensity. Calculate how many plants fall into this category and find their average Final_Chlorophyll value.

4. Create a boxplot comparing Photosynthesis_Rate across the three different Species (Arabidopsis, Tobacco, Spinach). Add appropriate colors and labels to make the plot publication-ready.

5. Calculate the correlation coefficient between Initial_Chlorophyll and Final_Chlorophyll. Test whether this correlation is statistically significant using cor.test().

6. Perform a t-test comparing the Chlorophyll_Change between plants grown under Low CO2 levels (400) versus High CO2 levels (1200). Interpret the results and state your biological conclusion.

---

**Thai Version:**

1. คำนวณค่าเฉลี่ย ค่ามัธยฐาน และส่วนเบี่ยงเบนมาตรฐานของค่า Initial_Chlorophyll สำหรับพืชทั้งหมดในชุดข้อมูล สร้างตารางสรุปแสดงสถิติเชิงพรรณนาเหล่านี้

2. สร้างฮิสโตแกรมของตัวแปร Photosynthesis_Rate พร้อมชื่อเรื่องและป้ายแกนที่เหมาะสม อธิบายว่าการแจกแจงนี้บอกอะไรเกี่ยวกับข้อมูล

3. ใช้ฟังก์ชัน filter() จาก dplyr เพื่อเลือกเฉพาะพืชที่มีแสงความเข้มสูง (High) คำนวณจำนวนพืชที่อยู่ในหมวดหมู่นี้และหาค่าเฉลี่ยของ Final_Chlorophyll

4. สร้างกราฟกล่องเปรียบเทียบ Photosynthesis_Rate ระหว่างสามสปีชีส์ (Arabidopsis, Tobacco, Spinach) เพิ่มสีและป้ายที่เหมาะสมให้กราฟพร้อมสำหรับการตีพิมพ์

5. คำนวณค่าสัมประสิทธิ์สหสัมพันธ์ระหว่าง Initial_Chlorophyll และ Final_Chlorophyll ทดสอบว่าสหสัมพันธ์นี้มีนัยสำคัญทางสถิติหรือไม่โดยใช้ cor.test()

6. ทำการทดสอบ t-test เปรียบเทียบ Chlorophyll_Change ระหว่างพืชที่ปลูกภายใต้ระดับ CO2 ต่ำ (400) เทียบกับระดับ CO2 สูง (1200) ตีความผลลัพธ์และระบุข้อสรุปทางชีววิทยา

---

## Dataset 2: Animal Behavioral Study
## ชุดข้อมูลที่ 2: การศึกษาพฤติกรรมสัตว์

**English Version:**

1. Create vectors containing the Weight_Gain values for each of the three species (Rat, Mouse, Hamster). Calculate the mean weight gain for each species and determine which species gained the most weight on average.

2. Use the select() function to create a new data frame containing only Animal_ID, Species, Diet_Type, and Activity_Score columns. Display the first 10 rows of this new data frame.

3. Create a scatter plot showing the relationship between Initial_Weight (x-axis) and Final_Weight (y-axis). Color the points by Species and add a legend to identify each species.

4. Filter the data to show only animals with Standard diet. Calculate the range (maximum minus minimum) of Activity_Score for these animals.

5. Create a boxplot comparing Activity_Score across the three different Diet_Type categories. Add appropriate colors and interpret what the plot reveals about the relationship between diet and activity.

6. Perform a t-test comparing Weight_Gain between animals fed High_Protein diet versus Low_Fat diet. Report the p-value and state whether there is a significant difference between these dietary treatments.

---

**Thai Version:**

1. สร้างเวกเตอร์ที่ประกอบด้วยค่า Weight_Gain สำหรับแต่ละสปีชีส์ทั้งสาม (Rat, Mouse, Hamster) คำนวณค่าเฉลี่ยการเพิ่มน้ำหนักของแต่ละสปีชีส์และหาว่าสปีชีส์ไหนที่เพิ่มน้ำหนักเฉลี่ยมากที่สุด

2. ใช้ฟังก์ชัน select() เพื่อสร้างเดตาเฟรมใหม่ที่มีเฉพาะคอลัมน์ Animal_ID, Species, Diet_Type และ Activity_Score แสดง 10 แถวแรกของเดตาเฟรมใหม่นี้

3. สร้างกราฟการกระจายแสดงความสัมพันธ์ระหว่าง Initial_Weight (แกน x) และ Final_Weight (แกน y) ระบายสีจุดตามสปีชีส์และเพิ่มคำอธิบายเพื่อระบุแต่ละสปีชีส์

4. กรองข้อมูลเพื่อแสดงเฉพาะสัตว์ที่ได้รับอาหารแบบ Standard คำนวณช่วง (ค่าสูงสุดลบค่าต่ำสุด) ของ Activity_Score สำหรับสัตว์เหล่านี้

5. สร้างกราฟกล่องเปรียบเทียบ Activity_Score ระหว่างสามประเภทของ Diet_Type เพิ่มสีที่เหมาะสมและตีความว่ากราฟเผยให้เห็นอะไรเกี่ยวกับความสัมพันธ์ระหว่างอาหารและกิจกรรม

6. ทำการทดสอบ t-test เปรียบเทียบ Weight_Gain ระหว่างสัตว์ที่ได้รับอาหาร High_Protein เทียบกับ Low_Fat รายงานค่า p-value และระบุว่ามีความแตกต่างอย่างมีนัยสำคัญระหว่างการรักษาด้วยอาหารเหล่านี้หรือไม่

---

## Dataset 3: Microbial Growth Experiment
## ชุดข้อมูลที่ 3: การทดลองการเจริญเติบโตของจุลินทรีย์

**English Version:**

1. Calculate the minimum, maximum, mean, and standard deviation of the Growth_Rate for all bacterial cultures. Create a summary table displaying these statistics with appropriate column names.

2. Use the arrange() function to sort the data frame by Growth_Rate in descending order. Display the top 8 cultures with the highest growth rates and identify their bacterial strains.

3. Create a histogram of the Final_OD600 values. Add a vertical line showing the mean Final_OD600 using the abline() function with appropriate color and line type.

4. Filter the data to show only cultures treated with Penicillin. Calculate how many cultures were included and find the average Growth_Time_Hours for this antibiotic treatment.

5. Create a boxplot comparing Initial_OD600 across the four different Bacterial_Strain categories. Use different colors for each strain and add appropriate axis labels.

6. Perform a t-test comparing Growth_Rate between cultures with no antibiotic treatment (None) versus cultures treated with Streptomycin. Interpret the biological significance of your findings.

---

**Thai Version:**

1. คำนวณค่าต่ำสุด ค่าสูงสุด ค่าเฉลี่ย และส่วนเบี่ยงเบนมาตรฐานของ Growth_Rate สำหรับเชื้อแบคทีเรียทั้งหมด สร้างตารางสรุปแสดงสถิติเหล่านี้พร้อมชื่อคอลัมน์ที่เหมาะสม

2. ใช้ฟังก์ชัน arrange() เพื่อเรียงลำดับเดตาเฟรมตาม Growth_Rate จากมากไปน้อย แสดง 8 เชื้อเพาะเลี้ยงแรกที่มีอัตราการเจริญเติบโตสูงสุดและระบุสายพันธุ์แบคทีเรียของพวกมัน

3. สร้างฮิสโตแกรมของค่า Final_OD600 เพิ่มเส้นตั้งแสดงค่าเฉลี่ยของ Final_OD600 โดยใช้ฟังก์ชัน abline() พร้อมสีและรูปแบบเส้นที่เหมาะสม

4. กรองข้อมูลเพื่อแสดงเฉพาะเชื้อเพาะเลี้ยงที่ได้รับการรักษาด้วย Penicillin คำนวณจำนวนเชื้อเพาะเลี้ยงที่รวมอยู่และหาค่าเฉลี่ยของ Growth_Time_Hours สำหรับการรักษาด้วยยาปฏิชีวนะนี้

5. สร้างกราฟกล่องเปรียบเทียบ Initial_OD600 ระหว่างสี่ประเภทของ Bacterial_Strain ใช้สีที่แตกต่างกันสำหรับแต่ละสายพันธุ์และเพิ่มป้ายแกนที่เหมาะสม

6. ทำการทดสอบ t-test เปรียบเทียบ Growth_Rate ระหว่างเชื้อเพาะเลี้ยงที่ไม่ได้รับยาปฏิชีวนะ (None) เทียบกับเชื้อเพาะเลี้ยงที่ได้รับการรักษาด้วย Streptomycin ตีความความสำคัญทางชีววิทยาของผลการค้นพบ

---

## Dataset 4: Seed Germination Study
## ชุดข้อมูลที่ 4: การศึกษาการงอกของเมล็ด

**English Version:**

1. Create a factor variable from the Soil_Type column and display the levels. Calculate the frequency table showing how many experimental groups were tested in each soil type.

2. Calculate the mean and median Germination_Percent for each Plant_Species. Create a summary table showing these statistics organized by species.

3. Create a scatter plot with Seeds_Germinated on the x-axis and Days_to_Germination on the y-axis. Color the points by Plant_Species and interpret the relationship you observe.

4. Use dplyr functions to filter the data for Tomato plants only, then arrange them by Germination_Percent in ascending order. Display the first 6 rows of this filtered and sorted data.

5. Create a boxplot comparing Days_to_Germination across the three Water_Frequency categories (Daily, Every_2_Days, Every_3_Days). Add appropriate colors and axis labels to enhance readability.

6. Perform a t-test comparing Germination_Rate between Daily watering versus Every_3_Days watering treatments. Calculate the correlation coefficient between Seeds_Planted and Seeds_Germinated and test its significance.

---

**Thai Version:**

1. สร้างตัวแปรแฟกเตอร์จากคอลัมน์ Soil_Type และแสดงระดับต่างๆ คำนวณตารางความถี่แสดงจำนวนกลุ่มทดลองที่ทดสอบในแต่ละประเภทของดิน

2. คำนวณค่าเฉลี่ยและค่ามัธยฐานของ Germination_Percent สำหรับแต่ละ Plant_Species สร้างตารางสรุปแสดงสถิติเหล่านี้จัดกลุ่มตามสปีชีส์

3. สร้างกราฟการกระจายโดยมี Seeds_Germinated ที่แกน x และ Days_to_Germination ที่แกน y ระบายสีจุดตาม Plant_Species และตีความความสัมพันธ์ที่สังเกตได้

4. ใช้ฟังก์ชัน dplyr เพื่อกรองข้อมูลเฉพาะพืชมะเขือเทศเท่านั้น จากนั้นเรียงลำดับตาม Germination_Percent จากน้อยไปมาก แสดง 6 แถวแรกของข้อมูลที่กรองและเรียงลำดับแล้ว

5. สร้างกราฟกล่องเปรียบเทียบ Days_to_Germination ระหว่างสามประเภทของ Water_Frequency (Daily, Every_2_Days, Every_3_Days) เพิ่มสีและป้ายแกนที่เหมาะสมเพื่อเพิ่มความอ่านง่าย

6. ทำการทดสอบ t-test เปรียบเทียบ Germination_Rate ระหว่างการให้น้ำทุกวัน เทียบกับการให้น้ำทุก 3 วัน คำนวณค่าสัมประสิทธิ์สหสัมพันธ์ระหว่าง Seeds_Planted และ Seeds_Germinated และทดสอบนัยสำคัญของมัน

---

## General Instructions for All Datasets
## คำแนะนำทั่วไปสำหรับทุกชุดข้อมูล

**English:**
- Use appropriate variable names and follow R coding best practices
- Include informative titles and axis labels for all plots
- Interpret statistical results in biological context
- Show all R code used to answer each question
- Round numerical results to appropriate decimal places (typically 2-3 digits)

**Thai:**
- ใช้ชื่อตัวแปรที่เหมาะสมและปฏิบัติตามแนวทางปฏิบัติที่ดีในการเขียนโค้ด R
- ใส่ชื่อเรื่องและป้ายแกนที่ให้ข้อมูลสำหรับกราฟทั้งหมด
- ตีความผลลัพธ์ทางสถิติในบริบททางชีววิทยา
- แสดงโค้ด R ทั้งหมดที่ใช้ตอบแต่ละคำถาม
- ปัดเศษผลลัพธ์ตัวเลขให้เหมาะสม (โดยทั่วไป 2-3 หลัก)

---