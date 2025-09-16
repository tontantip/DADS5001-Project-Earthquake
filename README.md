# DADS5001 Project Earthquake
Mini project DADS5001 Data Analytics and Data Science Tools and Programming.

## Table of Contents

- [Introduction](#introduction)
- [Data analytics](#data-analytics)
- [U](#usage)
- [Contributing](#contributing)

## Introduction

ในวันที่ 28 มีนาคม พ.ศ.2568 เกิดเหตุแผ่นดินไหวศูนย์กลางอยู่ในภาคซะไกง์ของประเทศพม่า แรงสั่นสะเทือนส่งผลกระทบถึงประเทศมีอาคาร ที่อยู่อาศัย ได้รับความเสียหายจำนวนมาก 
<div align="center">
  <img src="https://thestandard.co/wp-content/uploads/2025/05/SAO-Collapse.jpg?x62638" alt="SAO Collapse" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure1: อาคารสำนักการตรวจเงินแผ่นดินถล่ม.</em><br>
    ที่มา: <a href="https://thestandard.co/saocolapse/">The Standard</a>
  </p>
</div>
แผ่นดินไหวเป็นภัยที่ไม่สามารถทราบล่วงหน้าว่าจะเกิดขึ้นที่ไหนและเมื่อไรได้อย่างแน่นอน เนื่องจากสาเหตุที่เกิดการจากเคลื่อนตัวของแผ่นเปลือกโลกจากการสะสมของพลังงานเกิดแบบไม่สม่ำเสมอ ปัจจุบันสามารถทำได้เพียงคาดการณ์จากปัจจัยต่างที่มีแนวโน้มทำให้เกิดแผ่นดินไหวขึ้นเพียงเท่านั้น ดังนั้นการประเมินความเสี่ยงและเตรียมความพร้อมเพื่อลดความเสียหายจากภัยพิบัตินี้จึงเป็นสิ่งที่จำเป็น
</p>
ตั้งแต่ปี ค.ศ. 2005 ถึง เดือน สิงหาคม 2025 จากการรวมรวบสถิติเกิดแผ่นดินไหวทั่วโลก (Figure2) พบว่าจำนวนครั้งการเกิดแผ่นดินไหวแต่ละปีมีจำนวนครั้งไม่ต่ำกว่า 20 ครั้งในทุกขนาดความรุนแรงที่ปลดปล่อยออกมา หากพิจารณาเพียงจำนวนครั้งการเกิดแผ่นดินไหวไม่สามารถสรุปแนวโน้มแน่นอนได้ว่าเพิ่มขึ้นหรือลดลง แสดงให้เห็นว่าปัจจัยมีความซับซ้อนและหลากหลาย
</p>
<div align="center">
  <img src="https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/The%20number%20of%20earthquakes%20each%20year%20(2005-2025).png?raw=true" alt="SAO Collapse" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure2: Bar Chart แสดงจำนวนการเกิดแผนดินไหว (แกน Y: Earthquake Count) แต่ละปี ตั้งแต่ 2005-2025(เดือน สิงหาคม) (แกน X: Year(2005-2025)) ในแต่ละปีมีจำนวนแผ่นดอนไหวไม่ต่ำกว่า 20 ครั้ง และไม่มีแนวโน้มที่แน่นอน </em><br>
  </p>
</div>
หากวิเคราะห์การกระจายตัวของความรุนแผ่นดินไหวโดยตรง (มาตราวัดขนาด: Magnitude) หรือที่ทราบกันดีในหน่วย ริกเตอร์ สเกล (Richter scale) ตั้งแต่ปี 2005-2025 (Figure3) พบว่าการกระจายตัวใหญ่ (Median) จะอยู่ในช่วงความรุนแแรง 5.5 ถึง 6.5 ถึงเป็นความรุนแรงสามารถทำความเสียในบริเวณที่เป็นศูนย์กลางของการเกิดแผ่นดินไหวได้ ในปี 2011 มีค่า Outlier ความรุนแรงสูงมากเมื่อเทียบกับปีอื่นๆ ซึ่งมีขนาดถึง 9.0 ริกเตอร์ ซึ่งเป็นเหตุการณ์แผ่นไหวขนาด 9.0 ริกเตอร์ที่โทโฮคุ ประเทศญี่ปุ่น
</p>
<div align="center">
  <img src="https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/Dstnbution%20of%20Earthquake%20Magmtudes%20per%20Year%20(2005-2025).png?raw=true" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure3: Boxplot แสดงการกระจายของความรุนแรงแผ่นดินไหว (แกน Y: Magnitude) ในแต่ละปี (แกน X: Year 2005-2025) </em><br>
  </p>
</div>
</p>
<div align="center">
  <img src="https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/how_richter_scale_calculated.gif?raw=true" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure4: Understanding the Richter Scale </em><br>
    ที่มา: <a href="https://www.sms-tsunami-warning.com/">SMS tsunami warning</a>
  </p>
</div>
จากกราฟทั้ง 2 (Figure2 และ Figure3) ระหว่างจำนวนการเกิดแผ่นดินไหวและการกระจายตัวความรุนแรงของแผ่นดินไหว ตั้งแต่ปี 2005 ถึง 2025 พบว่า ในปีที่มีจำนวนครั้งเกิดแผ่นดินไหวไม่ได้หมายความว่าจะมีความรุนแรงมาก เช่นในปี 2008 (76 ครั้ง) แต่ค่า Median และค่า Outlier ความรุนแรงในปีดังกล่าวไม่สูงมาก  สอดคล้องกับกฎของ Gutenberg-Richter ซึ่งระบุว่า เมื่อขนาดความรุนแรงของแผ่นดินไหวเพิ่มขึ้น จำนวนครั้งที่เกิดขึ้นจะลดลงอย่างเป็นทวีคูณ (exponentially)
</p>
<div align="center">
  <img src="https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/Gutenberg-Richter%20Law.png?raw=true" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure5: Gutenberg Richter Law Chart </em><br>
    ที่มา: <a href="https://en.wikipedia.org/wiki/Gutenberg%E2%80%93Richter_law">Wikipedia</a>
  </p>
</div>
ปัญหาใหญ่ที่มาพร้อมกับการเกิดแผ่นไหวคือ ความสูญเสียไม่ว่าจะเป็นด้านชีวิต และ มูลค่า(จำนวนเงิน) โดยตั้งแต่ปี 2005 - 2025 ประเทศที่มีอัตราความเสียหายต่อจำนวนครั้งที่เกิดแผ่นดินไหวมากที่สุด 863.72 ล้านดอลล่า คือ ประเทศญี่ปุ่น (จำนวนกการเกิดแผ่นดินไหว 61 ครั้ง) จาก Figure6 ประเทศจีนมีจำนวนครั้งการเกิดแผ่นดินไหว 124 (มากที่สุดใหญ่) มีอัตราความเสียหายต่อจำนวนครั้ง 863.71 ล้านดอลล่า (อันดับที่ 9 ของโลก) ค่อยต่ำเมื่อเทียบกับจำนวนครั้งที่เกิดเหตุการณ์ อีกหนึ่งปัจจัยที่สำคัญและเป็นปัจจัยทางภูมิศาตร์คือ พื้นที่ของแต่ละประเทศ ประเทศจีนมีพื้นที่ 9,706,961 ตารางเมตร (มีพื้นที่มากเป็นอันดับ 1 ของโลก) ส่วนประเทศญี่ปุ่นมีพื้นที่ 377,930 ตารางเมตร (มีพื้นที่เป็นอันดับที่ 61 ของโลก) ข้อมูลนี้แสดงให้เห็นว่าพื้นที่ของประเทศและความหนาแน่นของประชากรเป็นปัจจัยที่มีผลต่ออัตราความเสียหายแม้มีจำนวนเหตุการณ์เกิดแผ่นดินไหวไม่มากก็สามารถมีอัตราความเสียหายต่อจำนวนเหตุการณ์ที่สูงได้ (จากเคสของประเทศญี่ปุ่น) 
</p>
<div align="center">
  <img src="https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/Total%20Damage%20per%20Event%20and%20Number%20of%20Event%20by%20Country%20(Top%2015).png?raw=true" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure6: กราฟแสดงข้อมูล Total Damage per Event Top 15 (อัตราความเสียหายต่อเหตุการณ์) และ Number of Events (จำนวนเหตุการณ์) ของประเทศ 15 อันดับแรก แกนY(ซ้าย) Damage per Event อัตราความเสียหายต่อเหตุการณ์ ($Mil/event) แกนY(ขวา)  Number of Event จำนวนเกิดเหตุการณ์แผ่นดินไหว แกนX Country ชื่อประเทศ </em><br>
    </p>
</div>
ถ้าพิจารณาอัตราความเสียหายต่อพื้นที่ของแต่ละประเทศ Figure7 สูงที่สุดคือประเทศญี่ปุ่น จำนวน 784.24 พันดอลล่าต่อตารางเมตร ที่เป็นประเทศที่เกิดเหตุการณ์บ่อย และอันดับของ 2 คือประเทศเฮติที่มีอัตราความเสียหาย 348.65 พันดอลล่าต่อตารางเมตร เนื่องจากประเทศเฮติมีพื้นที่ประเทศ 27,750 ตารางเมตร (อันดับที่ 146 ของโลก) จัดเป็นประเทศที่มีขนาดเล็ก ดังนั้นปัจจัยที่มีผลต่ออัตราความเสีย ได้แก่ จำนวนเหตุการณ์เกิดแผ่นดินไหว, พื้นที่ของประเทศ และ ความหนาแน่นของประชากร เป็นต้น
  </p>
</div>
</p>
<div align="center">
  <img src="https://raw.githubusercontent.com/tontantip/DADS5001-Project-Earthquake/refs/heads/main/image/Total%20Damage%20per%20Area%20by%20Country%20(Top%2020).png" width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure7: กราฟแสดงข้อมูล Total Damage per Area by Country (อัตราความเสียหายรวมต่อพื้นที่) แกนX Damage per Area อัตราความเสียหายต่อพื้นที่ ($k/square meter) แกนX Country ชื่อประเทศ </em><br>
  </p>
</div>
มูลค่าความเสียหายเป็นจำนวนเงินสูงที่ประเทศต่อแบกรับ สำหรับประเทศไทยมีอัตราความเสียหายต่อเหตุการณ์เกิดแผ่นดินไหว 393.12 ล้านดอลล่า (อันดับที่ 12 ของโลก) และอัตราความเสียหายต่อพื้นที่ตารางเมตร 3.83 พันดอลล่า (อันดับที่ 17 ของโลก) นับเป็นจำนวนเงินที่สูงมากที่ต้องสูญเสียไปกับการเกิดเหตุการณ์แผ่นดินไหว ทำให้ประเทศสูญเสียงบประมาณและเสียโอกาสในการพัฒนาประเทศไทย ดังนั้นการบริหารความเสี่ยง เช่น เมื่อเกิดเหตุแผ่นดินไหวพื้นที่ไหนมีความเสียหายมาก, สิ่งปลูกสร้างประเภทไหนที่เสี่ยงจะเสียหาย พิจารณาร่วมกับปัจจัยต่างๆเพื่อบริหารความเสี่ยง สามารถลดอัตราความสูญเสียในอนาคตได้

## Data analytics
วิเคราะห์จากข้อมูลแจ้งความเสียหายพบว่าโครงสร้างของคอนโดมิเนียม 5,865 ครั้ง มีจำนวนการแจ้งความเสียหายเข้ามามากที่สุดเป็นอันดับหนึ่ง ตามมาด้วย บ้าน (2,432 ครั้ง) คิดเป็น 70% ของจำนวนการแจ้งความเสียหายทั้งหมด และในขณะเดียวกันจำนวนจากคอนโดมิเนียม มากกว่าขึ้น 2 เท่าของอันดับ 2 อย่างบ้าน Figure8
</p>
</div>
</p>
<div align="center">
  <img src=https://github.com/tontantip/DADS5001-Project-Earthquake/blob/main/image/Total%20Reported%20Damages%20by%20Building%20Type.png?raw=true width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure8: กราฟแสดงข้อมูล Total Reported Damages by Building Type (จำนวนการแจ้งความเสียหาย) แกนX Building Type ประเภทสิ่งปลูกสร้าง แกนY Reported Damage จำนวนแจ้งความเสียหาย </em><br>
  </p>
</div>
สิ่งที่น่าสนใจคือ จำนวนที่มีการแจ้งความเสียหายหลังจากการตรวจสอบแล้วไม่พบความเสียหาย คอนโดมิเนียมมีมากที่สุดจำนวน 726 ครั้ง คิดเป็น 6.17% ของจำนวนแจ้งทั้งหมด Figure9 ดังนั้นปัจจัยที่ทำให้จำนวนการแจ้งจากคอนโดมิเนียมสูงมาก อาจจะมีดังนี้
</p>
</div>
</p>
<div align="center">
  <img src=https://raw.githubusercontent.com/tontantip/DADS5001-Project-Earthquake/refs/heads/main/image/Number%20of%20Damage%20Reports%20Verified%20as%20_No%20Damage%20Found_%20by%20Building%20Type.png width="500">
  <p style="font-size: 0.9em; color: #555;">
    <em>Figure9: กราฟแสดงข้อมูล Number of Damage Reports Verified as "No Damage Found" by Building Type (จำนวนรายงานความเสียหายที่ตรวจสอบแล้วไม่พบความเสียหายจำแนกตามประเภทสิ่งปลูกสร้าง) แกนX Number of Verified No-Damage Reports จำนวนแจ้งที่ไม่พบความเสียหาย แกนY Building Type ประเภทสิ่งปลูกสร้าง </em><br>
  </p>
</div>
### Prerequisites

ก่อนการติดตั้ง คุณต้องมี...

### Steps

1.  โคลน repository:
    `git clone https://github.com/your-username/your-project.git`
2.  ติดตั้ง dependencies:
    `npm install`

## Usage

วิธีการใช้งานโปรเจกต์นี้...

## Contributing

ยินดีรับการมีส่วนร่วม! หากคุณต้องการช่วยพัฒนา...
