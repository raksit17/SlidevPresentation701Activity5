
  <template>
    <div class="green-layout">
      <div class="content-box">
        <h1>Natural Language Commanding via Program Synthesis</h1>
        <div class="section">
          <h2 class="section-title"> Problem</h2>
          <hr class="section-divider" />
          <ul>
            <li>การแปลงภาษาธรรมชาติเป็นคำสั่ง Bash เป็นเรื่องท้าทายเพราะความกำกวมของภาษาและความหลากหลายของคำสั่ง Bash พร้อมกับข้อจำกัดของข้อมูลคู่ที่มีอยู่น้อยมาก</li>
          
          </ul>
        </div>
       <div class="section">
       <h2 class="section-title"> Methodology</h2>
       <hr class="section-divider" />
        <div class="sub-section">
          <h2 class="sub-section-title">Model Development</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ใช้ Back-translation สร้างคู่ข้อมูลระหว่าง Bash Commands และภาษาธรรมชาติ พัฒนาโมเดล Transformer เป็นทั้งตัวเข้ารหัสและถอดรหัส เน้นลดขนาดคำศัพท์ผ่านการแทนค่าตัวแปรและใช้ Ensemble รวมผลลัพธ์จากโมเดลที่แม่นยำที่สุด เพื่อเพิ่มความแม่นยำและรองรับคำสั่ง Bash ที่หลากหลาย
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">Validation and Post-Processingn</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ตรวจสอบคำสั่ง Bash ในสภาพแวดล้อมเสมือนและใช้ Post-processing เพื่อแทนค่าตัวแปรด้วยข้อมูลจริงให้คำสั่งพร้อมใช้งาน
            </li>
          </ul>
        </div>
   
        <div class="sub-section">
          <h2 class="sub-section-title">ChatGPT Integration</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ใช้ ChatGPT สร้างชุดข้อมูล Bash Commands และคู่ภาษาธรรมชาติ ลดเวลาสร้างข้อมูลจากสองเดือนเหลือสามวันพร้อมเพิ่มความหลากหลายและคุณภาพข้อมูล
            </li>
          </ul>
        </div>
      </div>
      <div class="section">
        <h2 class="section-title"> Result</h2>
        <hr class="section-divider" />
        <ul>
          <li>ชุดข้อมูล NL2CMD ที่สร้างขึ้นใหม่ใหญ่กว่าชุดเดิม 6 เท่าและมีความหลากหลายมากขึ้น โมเดล Transformer มีความแม่นยำสูงสุด 53.2% บนชุดข้อมูลเดิมและ 31.6% บนชุดข้อมูลใหม่ พร้อมปรับปรุงด้วย ChatGPT</li>
        
        </ul>
      </div>
      <div class="section">
        <h2 class="section-title"> Remaining problems</h2>
        <hr class="section-divider" />
        <ul>
          <li>ยังคงมีความท้าทายในการสร้างโมเดลที่สามารถทั่วไปกับข้อมูลชุดใหม่และการแก้ปัญหาความกำกวมในการแปลงคำสั่งที่ซับซ้อน</li>
        
        </ul>
      </div>
      </div>
    
    </div>
  </template>
  


<style scoped>
.icon {
  margin-right: 10px;
  background: linear-gradient(90deg, #8fe114, #f4d03f);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.green-layout {
  background-image: url('/assets/images/pexels-goumbik-1420709.jpg'); /* พื้นหลัง */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color: white;
  height: 100vh; /* ครอบคลุมหน้าจอ */
  width: 100%;
  display: flex;
  flex-direction: column;

  align-items: center;
  text-align: left; /* ข้อความชิดซ้าย */
  padding: 20px;
  box-sizing: border-box;
}

.content-box {
  background-color: rgba(0, 0, 0, 0.8); /* พื้นหลังโปร่งแสง */
  padding: 9px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3); /* เพิ่มเงา */
  max-width: 1000px;
  width: 100%; /* กำหนดกว้างสุด */

  color: #f8f6ad;

  height: 60%;
}

h1 {
  font-size: 1.2rem;
  margin-bottom: 20px;
  text-align: left; /* หัวข้อใหญ่จัดกึ่งกลาง */
  color: #eceeef; /* สีเน้นของหัวข้อใหญ่ */
}
.section {
  margin-bottom: 0px; /* เพิ่มระยะห่างระหว่างแต่ละ section */
  padding: 1px 1px 1px 1px;
 
  border-radius: 8px; /* มุมโค้งมน */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* เพิ่มเงาเพื่อแยกส่วน */
}
.section-title {
  font-size: 0.8rem;
  color: #f1ee60; /* สีเน้นของหัวข้อย่อย */
  margin: 10px 0;
}

.sub-section {
  margin-top: 0px;
  padding-left: 15px;
  padding-top: 1px;
}

.sub-section-title {
  font-size: 0.7rem;
  color:  #f1ee60;
  margin-bottom: 10px;
}

.section-divider {
  border: 0;
  border-top: 2px solid #ffffff; /* เส้นแบ่งหัวข้อ */
  margin: 1px 0 5px;
}

ul {
  margin: 0;
  padding-left: 20px;
}

ul ul {
  margin: 5px 0;
}

li {
  font-size: 0.7rem; /* ลดขนาดฟอนต์ */
  margin-bottom: 6px; /* ลดระยะห่างระหว่างรายการ */
  line-height: 1.4; /* ลดระยะห่างระหว่างบรรทัด */
}
</style>
