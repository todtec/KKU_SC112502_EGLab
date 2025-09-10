# เอกสารประกอบปฏิบัติการ: Basic R Programming and Chi-square Analysis

## บทที่ 1: บทนำ (Introduction)

### 1.1 พื้นฐานความรู้ทางสถิติชีววิทยา (Statistical Biology Foundation)

การวิเคราะห์ข้อมูลทางชีววิทยาในยุคปัจจุบันต้องอาศัยเครื่องมือทางสถิติที่มีประสิทธิภาพและความแม่นยำสูง โดยเฉพาะอย่างยิ่งในการทดสอบสมมติฐานทางพันธุศาสตร์ (Sokal & Rohlf, 2012) ภาษา R ถือเป็นเครื่องมือมาตรฐานในการวิเคราะห์ข้อมูลทางชีววิทยาเชิงคำนวณ (Computational Biology) ด้วยความสามารถในการจัดการข้อมูลขนาดใหญ่และการวิเคราะห์ทางสถิติที่หลากหลาย

### 1.2 หลักการทางพันธุศาสตร์ของเมนเดล (Mendelian Genetics Principles)

กฎของเมนเดล (Mendel's Laws) ประกอบด้วยกฎการแยกตัว (Law of Segregation) และกฎการรวมกลุ่มอิสระ (Law of Independent Assortment) ซึ่งเป็นพื้นฐานสำคัญในการทำความเข้าใจการถ่ายทอดลักษณะทางพันธุกรรม (Hartl & Clark, 2007)

#### 1.2.1 Monohybrid Cross
การผสมพันธุ์แบบลักษณะเดียว แสดงอัตราส่วนฟีโนไทป์ 3:1 ในรุ่น F2 ตามทฤษฎี

#### 1.2.2 Dihybrid Cross  
การผสมพันธุ์แบบสองลักษณะ แสดงอัตราส่วนฟีโนไทป์ 9:3:3:1 ในรุ่น F2 ตามทฤษฎี

### 1.3 การทดสอบไคสแควร์ (Chi-square Test)

การทดสอบไคสแควร์เป็นวิธีการทางสถิติที่ใช้ในการทดสอบความสอดคล้องระหว่างค่าที่สังเกตได้ (Observed values) กับค่าที่คาดหวังตามทฤษฎี (Expected values) โดยมีสูตรการคำนวณดังนี้:

**χ² = Σ[(O - E)² / E]**

โดยที่:
- O = ค่าที่สังเกตได้ (Observed frequency)
- E = ค่าที่คาดหวัง (Expected frequency)

### 1.4 ภาษา R และ RStudio

R เป็นภาษาโปรแกรมเชิงสถิติแบบ open-source ที่พัฒนาโดย R Core Team (2023) มีความสามารถในการจัดการข้อมูล การวิเคราะห์ทางสถิติ และการสร้างกราฟิกคุณภาพสูง RStudio เป็น Integrated Development Environment (IDE) ที่ช่วยให้การเขียนโปรแกรม R มีประสิทธิภาพมากขึ้น

## บทที่ 2: วัตถุประสงค์ของปฏิบัติการ (Laboratory Objectives)

### 2.1 วัตถุประสงค์หลัก (Primary Objectives)
1. พัฒนาความเข้าใจพื้นฐานการเขียนโปรแกรมภาษา R และการใช้งาน RStudio
2. ประยุกต์ใช้การทดสอบไคสแควร์ในการวิเคราะห์ข้อมูลทางพันธุศาสตร์
3. ตรวจสอบความสอดคล้องของผลการทดลองกับกฎของเมนเดล

### 2.2 วัตถุประสงค์รอง (Secondary Objectives)
1. พัฒนาทักษะการนำเข้าและส่งออกข้อมูลระหว่าง R และ Excel
2. สร้างความเข้าใจในการจัดการข้อมูลแบบตาราง (Data frame manipulation)
3. พัฒนาความสามารถในการแปลผลทางสถิติในบริบทชีววิทยา

## บทที่ 3: วัสดุอุปกรณ์ (Materials and Equipment)

### 3.1 ฮาร์ดแวร์ (Hardware Requirements)
- คอมพิวเตอร์ที่มี RAM อย่างน้อย 4 GB
- พื้นที่จัดเก็บข้อมูลอย่างน้อย 2 GB

### 3.2 ซอฟต์แวร์ (Software Requirements)
- R version 4.0 หรือสูงกว่า (https://www.r-project.org/)
- RStudio Desktop (https://www.rstudio.com/products/rstudio/download/)
- Microsoft Excel หรือ LibreOffice Calc
- Web browser สำหรับเข้าถึงเอกสารออนไลน์

### 3.3 ข้อมูลสำหรับการวิเคราะห์ (Data Files)
- ไฟล์ข้อมูลตัวอย่าง Monohybrid cross (จะสร้างในปฏิบัติการ)
- ไฟล์ข้อมูลตัวอย่าง Dihybrid cross (จะสร้างในปฏิบัติการ)

## บทที่ 4: กิจกรรมปฏิบัติการ (Laboratory Activities)

### กิจกรรมที่ 1: การติดตั้งและเริ่มต้นใช้งาน R และ RStudio (30 นาที)

#### ขั้นตอนที่ 1.1: การตรวจสอบการติดตั้ง
```r
# ตรวจสอบเวอร์ชันของ R
R.version.string

# ตรวจสอบ working directory
getwd()

# กำหนด working directory (แก้ไขตามเครื่องของผู้ใช้)
setwd("~/Documents/R_Lab")
```

#### ขั้นตอนที่ 1.2: การติดตั้ง packages ที่จำเป็น
```r
# ติดตั้ง packages สำหรับการจัดการข้อมูล
install.packages("readxl")    # สำหรับอ่านไฟล์ Excel
install.packages("writexl")   # สำหรับเขียนไฟล์ Excel
install.packages("tidyverse") # สำหรับจัดการข้อมูล

# โหลด packages
library(readxl)
library(writexl)
library(tidyverse)
```

### กิจกรรมที่ 2: พื้นฐานการเขียนโปรแกรม R (45 นาที)

#### ขั้นตอนที่ 2.1: การสร้างและจัดการตัวแปร (Variables)
```r
# การสร้างตัวแปรชนิดต่างๆ
gene_name <- "BRCA1"                    # Character
chromosome_number <- 17                 # Numeric
is_dominant <- TRUE                     # Logical
alleles <- c("A", "a")                 # Vector
phenotype_ratio <- c(3, 1)             # Numeric vector

# แสดงผลตัวแปร
print(gene_name)
print(paste("Chromosome:", chromosome_number))
print(paste("Dominant allele:", is_dominant))
```

#### ขั้นตอนที่ 2.2: การสร้าง Data Frame
```r
# สร้าง data frame สำหรับข้อมูล Monohybrid cross
monohybrid_data <- data.frame(
  Phenotype = c("Tall", "Dwarf"),
  Observed = c(787, 277),
  Expected_Ratio = c(3, 1)
)

# คำนวณค่าที่คาดหวัง
total_plants <- sum(monohybrid_data$Observed)
monohybrid_data$Expected <- total_plants * 
  monohybrid_data$Expected_Ratio / 
  sum(monohybrid_data$Expected_Ratio)

# แสดงผลข้อมูล
print(monohybrid_data)
```

### กิจกรรมที่ 3: การนำเข้าและส่งออกข้อมูล Excel (30 นาที)

#### ขั้นตอนที่ 3.1: การสร้างข้อมูลตัวอย่างและส่งออกเป็น Excel
```r
# สร้างข้อมูล Dihybrid cross
dihybrid_data <- data.frame(
  Phenotype = c("Round-Yellow", "Round-Green", 
                "Wrinkled-Yellow", "Wrinkled-Green"),
  Observed = c(315, 108, 101, 32),
  Expected_Ratio = c(9, 3, 3, 1)
)

# คำนวณค่าที่คาดหวัง
total_seeds <- sum(dihybrid_data$Observed)
dihybrid_data$Expected <- total_seeds * 
  dihybrid_data$Expected_Ratio / 16

# บันทึกเป็นไฟล์ Excel
write_xlsx(dihybrid_data, "dihybrid_cross_data.xlsx")
print("File saved successfully!")
```

#### ขั้นตอนที่ 3.2: การอ่านข้อมูลจาก Excel
```r
# อ่านข้อมูลจากไฟล์ Excel
imported_data <- read_excel("dihybrid_cross_data.xlsx")

# ตรวจสอบโครงสร้างข้อมูล
str(imported_data)
summary(imported_data)
head(imported_data)
```

### กิจกรรมที่ 4: การวิเคราะห์ Chi-square สำหรับ Monohybrid Cross (35 นาที)

#### ขั้นตอนที่ 4.1: การคำนวณ Chi-square แบบ Manual
```r
# ใช้ข้อมูล Monohybrid cross
observed <- c(787, 277)
expected <- c(798, 266)  # คำนวณจากอัตราส่วน 3:1

# คำนวณ Chi-square
chi_square <- sum((observed - expected)^2 / expected)
print(paste("Chi-square value:", round(chi_square, 4)))

# กำหนด degrees of freedom
df <- length(observed) - 1
print(paste("Degrees of freedom:", df))

# หา p-value
p_value <- pchisq(chi_square, df, lower.tail = FALSE)
print(paste("P-value:", round(p_value, 4)))

# การแปลผล
alpha <- 0.05
if(p_value > alpha) {
  print("ไม่ปฏิเสธสมมติฐานหลัก: ข้อมูลสอดคล้องกับอัตราส่วน 3:1")
} else {
  print("ปฏิเสธสมมติฐานหลัก: ข้อมูลไม่สอดคล้องกับอัตราส่วน 3:1")
}
```

#### ขั้นตอนที่ 4.2: การใช้ฟังก์ชัน chisq.test()
```r
# การทดสอบโดยใช้ฟังก์ชันสำเร็จรูป
result_mono <- chisq.test(x = observed, 
                          p = c(3/4, 1/4))

# แสดงผลลัพธ์
print(result_mono)

# ดึงค่าสถิติที่สำคัญ
print(paste("Chi-square statistic:", result_mono$statistic))
print(paste("P-value:", result_mono$p.value))
print(paste("Expected frequencies:", 
            paste(result_mono$expected, collapse = ", ")))
```

### กิจกรรมที่ 5: การวิเคราะห์ Chi-square สำหรับ Dihybrid Cross (40 นาที)

#### ขั้นตอนที่ 5.1: การเตรียมข้อมูลและการวิเคราะห์
```r
# ข้อมูล Dihybrid cross ของ Mendel
observed_dihy <- c(315, 108, 101, 32)
expected_ratio <- c(9, 3, 3, 1)
expected_prob <- expected_ratio / sum(expected_ratio)

# ทดสอบ Chi-square
result_dihy <- chisq.test(x = observed_dihy, 
                          p = expected_prob)

# สร้างตารางสรุปผล
summary_table <- data.frame(
  Phenotype = c("Round-Yellow", "Round-Green", 
                "Wrinkled-Yellow", "Wrinkled-Green"),
  Observed = observed_dihy,
  Expected = result_dihy$expected,
  Chi_square_component = (observed_dihy - result_dihy$expected)^2 / 
                         result_dihy$expected
)

print(summary_table)
print(paste("Total Chi-square:", sum(summary_table$Chi_square_component)))
print(paste("P-value:", result_dihy$p.value))
```

#### ขั้นตอนที่ 5.2: การสร้างกราฟเปรียบเทียบ
```r
# เตรียมข้อมูลสำหรับการ plot
comparison_data <- data.frame(
  Phenotype = rep(c("R-Y", "R-G", "W-Y", "W-G"), 2),
  Count = c(observed_dihy, result_dihy$expected),
  Type = rep(c("Observed", "Expected"), each = 4)
)

# สร้าง barplot เปรียบเทียบ
barplot(matrix(comparison_data$Count, nrow = 2, byrow = TRUE),
        beside = TRUE,
        names.arg = c("R-Y", "R-G", "W-Y", "W-G"),
        col = c("lightblue", "lightgreen"),
        legend.text = c("Observed", "Expected"),
        main = "Dihybrid Cross: Observed vs Expected",
        xlab = "Phenotype",
        ylab = "Frequency")
```

### กิจกรรมที่ 6: การสร้างฟังก์ชันสำหรับการวิเคราะห์อัตโนมัติ (30 นาที)

```r
# สร้างฟังก์ชันสำหรับการวิเคราะห์ Mendelian ratio
analyze_mendelian_ratio <- function(observed, expected_ratio, alpha = 0.05) {
  # คำนวณค่าที่คาดหวัง
  total <- sum(observed)
  expected_prob <- expected_ratio / sum(expected_ratio)
  
  # ทดสอบ Chi-square
  test_result <- chisq.test(x = observed, p = expected_prob)
  
  # สร้างตารางผลลัพธ์
  results <- list(
    observed = observed,
    expected = test_result$expected,
    chi_square = test_result$statistic,
    df = test_result$parameter,
    p_value = test_result$p.value,
    conclusion = ifelse(test_result$p.value > alpha,
                       "Data consistent with expected ratio",
                       "Data inconsistent with expected ratio")
  )
  
  return(results)
}

# ทดสอบฟังก์ชัน
mono_test <- analyze_mendelian_ratio(c(787, 277), c(3, 1))
print(mono_test)

dihy_test <- analyze_mendelian_ratio(c(315, 108, 101, 32), c(9, 3, 3, 1))
print(dihy_test)
```

## บทที่ 5: ตารางบันทึกผลการทดลอง (Data Recording Tables)

### ตาราง 5.1: ผลการวิเคราะห์ Monohybrid Cross

| Parameter | Value | Interpretation |
|-----------|-------|----------------|
| Observed Tall | | |
| Observed Dwarf | | |
| Expected Tall | | |
| Expected Dwarf | | |
| Chi-square Statistic | | |
| Degrees of Freedom | | |
| P-value | | |
| Conclusion (α = 0.05) | | |

### ตาราง 5.2: ผลการวิเคราะห์ Dihybrid Cross

| Phenotype | Observed | Expected | (O-E)²/E | 
|-----------|----------|----------|----------|
| Round-Yellow | | | |
| Round-Green | | | |
| Wrinkled-Yellow | | | |
| Wrinkled-Green | | | |
| **Total** | | | |

### ตาราง 5.3: สรุปผลการทดสอบสมมติฐาน

| Test Type | H₀ | H₁ | Chi-square | df | P-value | Decision |
|-----------|----|----|------------|----|---------| ---------|
| Monohybrid | Ratio = 3:1 | Ratio ≠ 3:1 | | | | |
| Dihybrid | Ratio = 9:3:3:1 | Ratio ≠ 9:3:3:1 | | | | |

## บทที่ 6: คำถามท้ายบท (Post-Laboratory Questions)

### ส่วนที่ 1: คำถามเชิงทฤษฎี (Theoretical Questions)

1. **อธิบายความแตกต่างระหว่างค่า Chi-square ที่คำนวณได้กับค่า Critical value** พร้อมทั้งระบุความสำคัญของการเปรียบเทียบค่าทั้งสองในการทดสอบสมมติฐานทางสถิติ (อย่างน้อย 150 คำ)

2. **วิเคราะห์ผลกระทบของขนาดตัวอย่าง (Sample size) ต่อการทดสอบ Chi-square** ในการทดลองทางพันธุศาสตร์ พร้อมยกตัวอย่างประกอบ

3. **จงอธิบายข้อจำกัดของการทดสอบ Chi-square** ในการวิเคราะห์ข้อมูลทางพันธุศาสตร์ และเสนอแนวทางการแก้ไขหรือวิธีการทดสอบทางเลือก

### ส่วนที่ 2: คำถามเชิงปฏิบัติ (Practical Questions)

4. **จงเขียนโค้ด R เพื่อจำลองการทดลอง Monohybrid cross** โดยสุ่มตัวอย่าง 1000 ต้น และทดสอบว่าผลที่ได้สอดคล้องกับอัตราส่วน 3:1 หรือไม่

5. **หากผลการทดสอบ Chi-square ให้ค่า p-value = 0.03** จงอธิบายการแปลผลในบริบทของการทดลองทางพันธุศาสตร์ และข้อควรพิจารณาในการสรุปผล

6. **จงสร้างฟังก์ชัน R ที่สามารถ:**
   - รับข้อมูล observed frequencies
   - คำนวณ expected frequencies จาก Mendelian ratio
   - ทำการทดสอบ Chi-square
   - สร้างกราฟเปรียบเทียบ observed vs expected
   - ส่งออกผลลัพธ์เป็นไฟล์ Excel

### ส่วนที่ 3: คำถามเชิงวิเคราะห์ (Analytical Questions)

7. **วิเคราะห์กรณีศึกษา:** หากการทดลอง Dihybrid cross ให้ผลที่ไม่สอดคล้องกับอัตราส่วน 9:3:3:1 จงเสนอสมมติฐานทางชีววิทยาที่เป็นไปได้อย่างน้อย 3 ข้อ พร้อมวิธีการทดสอบสมมติฐานเหล่านั้น

8. **การประยุกต์ใช้:** จงออกแบบการทดลองทางพันธุศาสตร์ที่ใช้การทดสอบ Chi-square ในการวิเคราะห์ผล โดยระบุ:
   - วัตถุประสงค์ของการทดลอง
   - ขนาดตัวอย่างที่เหมาะสม
   - วิธีการเก็บข้อมูล
   - การวิเคราะห์ทางสถิติ
   - การแปลผลและข้อจำกัด

## บทที่ 7: ภาคผนวก (Appendices)

### ภาคผนวก ก: ตาราง Critical Values ของ Chi-square

| df | α = 0.10 | α = 0.05 | α = 0.01 | α = 0.001 |
|----|----------|----------|----------|-----------|
| 1  | 2.706    | 3.841    | 6.635    | 10.828    |
| 2  | 4.605    | 5.991    | 9.210    | 13.816    |
| 3  | 6.251    | 7.815    | 11.345   | 16.266    |
| 4  | 7.779    | 9.488    | 13.277   | 18.467    |
| 5  | 9.236    | 11.070   | 15.086   | 20.515    |

### ภาคผนวก ข: R Commands Quick Reference

```r
# Basic Operations
c()                 # Create vector
data.frame()        # Create data frame
sum()              # Sum values
mean()             # Calculate mean
sd()               # Standard deviation

# Data Import/Export
read_excel()       # Read Excel file
write_xlsx()       # Write Excel file
read.csv()         # Read CSV file
write.csv()        # Write CSV file

# Statistical Tests
chisq.test()       # Chi-square test
pchisq()           # Chi-square distribution
qchisq()           # Chi-square quantile

# Graphics
plot()             # Basic plot
barplot()          # Bar plot
hist()             # Histogram
```

### ภาคผนวก ค: Troubleshooting Guide

| Problem | Possible Cause | Solution |
|---------|---------------|----------|
| Package not found | Package not installed | Use install.packages() |
| Cannot find file | Wrong working directory | Use setwd() or full path |
| Unexpected symbol | Syntax error | Check brackets and quotes |
| Object not found | Variable not defined | Check spelling and run previous code |

## เอกสารอ้างอิง (References)

1. Hartl, D. L., & Clark, A. G. (2007). *Principles of Population Genetics* (4th ed.). Sinauer Associates.

2. R Core Team. (2023). *R: A Language and Environment for Statistical Computing*. R Foundation for Statistical Computing. https://www.R-project.org/

3. Sokal, R. R., & Rohlf, F. J. (2012). *Biometry: The Principles and Practice of Statistics in Biological Research* (4th ed.). W.H. Freeman.

4. Wickham, H., & Grolemund, G. (2017). *R for Data Science*. O'Reilly Media.

5. Zar, J. H. (2010). *Biostatistical Analysis* (5th ed.). Pearson Prentice Hall.

---
*เอกสารประกอบปฏิบัติการนี้จัดทำขึ้นสำหรับนักศึกษาระดับปริญญาตรี สาขาชีววิทยา*  
*ระยะเวลาปฏิบัติการ: 3 ชั่วโมง*