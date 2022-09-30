# Recommendation
### 1. การออกแบบระบบแนะนำ
  โดยจากการศึกษาการทำระบบแนะนำจากงานวิจัยต่างๆ ทำให้ได้ข้อสรุปว่าเราจะใช้วิธีแนะนำทั้งหมด 3 แบบได้แก่
  1. Demographic filtering คือระบบแนะนำที่ใช้ข้อมูลโปรไฟล์ของผู้ใช้ โดยตัวอย่างข้อมูลที่ใช้เช่น ข้อมูลเพศ อายุของผู้ใช้เป็นต้น จึงทำให้ระบบแนะนำนี้ เหมาะมากกับการนำมาแก้ปัญหาผู้ใช้ใหม่ในระบบ
  2. Collaborative filtering คีอระบบแนะนำที่ใช้ข้อมูลการรีวิวสถานที่ของผู้ใช้ ทำให้เหมาะกับผู้ใช้ที่มีประวัติการรีวิวแล้วเท่านั้นค่ะ ซึ่งวิธีนี้นะคะ จะช่วยในการแนะนำสถานที่ได้อย่างหลากหลาย และไม่จำเจ
  3. Hybrid recommender system จะเห็นว่าระบบแนะนำทั้งสองมีจุดประสงค์ที่ใช้งานต่างกัน เราจึงเลือกใช้ Hybrid recommender system มาช่วยในการเลือกใช้วิธีแนะนำค่ะ โดยใช้เทคนิค Switching hybrid คือการตรวจสอบว่าผู้ใช้เป็นผู้ใช้ใหม่หรือไม่ หากใช่เราจะใช้ Demographic filtering  และหากตรวจสอบได้ว่าผู้ใช้มีประวัติการรีวิวสถานที่แล้วจะใช้วิธี Collaborative filtering ค่ะ ซึ่งผลลัพธ์คือ อันดับสถานที่ที่ได้คะแนนสูงสุดจากการทำนาย
### 2. การออกแบบการวิเคราะห์ข้อมูล
  1. การรวบรวมชุดข้อมูล เนื่องจากชุดข้อมูลถูกแบ่งออกเป็น 2 ชุดดังนั้นในการเก็บข้อมูลจะถูกแบ่งออกไปคนละแบบและคนละช่วงเวลาในการใช้แอปพลิเคชัน
    - ข้อมูลชุดแรกใช้ในการทำการกรองข้อมูลแบบประชากรศาสตร์ จะถูกเก็บเมื่อผู้ใช้เริ่มต้นการใช้งานแอปพลิเคชันครั้งแรก
    - ข้อมูลชุดที่สองใช้ในการกรองข้อมูลแบบพึ่งพาผู้ใช้ร่วม โดยข้อมูลจะถูกเก็บเมื่อผู้ใช้มีการรีวิวหรือให้คะแนนสถานที่ เพื่อนำข้อมูลการให้คะแนนสถานที่ของผู้ใช้ไปใช้การทำนายว่ามีผู้ใช้คนไหนที่มีการให้คะแนนสถานที่คล้ายกันมากสุด จากนั้นจึงนำสถานที่ที่ผู้ใช้ที่มีการให้คะแนนสถานที่ที่ผู้ใช้เป้าหมายไม่เคยให้คะแนนไปแนะนำ
  2. การทำความสะอาดข้อมูล คือการทำความสะอาดข้อมูลที่นำเข้ามาทำระบบแนะนำ ในการ คัดข้อมูลที่ไม่เกี่ยวข้องออกไป
  3. การแปลงข้อมูล เป็นการแปลงข้อมูลให้เหมาะสมกับการใช้งาน ก่อนนำไปทำระบบแนะนำเนื่องจากบางระบบแนะนำไม่สามารถคำนวณข้อมูลที่เป็นตัวอักษรได้ หรือบางข้อมูลควรมีการ Normalize ข้อมูลก่อนนำไป
 ### 3. เครื่องมือที่ใช้ ซึ่งใช้ Python ในการพัฒนา
    - Google Colab
    - Visual Studio Code
 ### 4. Library
    - Pandas
    - NumPy
    - Scikit-learn
    - Fastapi
 
 
