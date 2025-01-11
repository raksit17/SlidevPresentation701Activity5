
  <template>
    <div class="green-layout">
      <div class="content-box">
        <h1>Natural Language Commanding via Program Synthesis</h1>
        <div class="section">
          <h2 class="section-title"> Problem</h2>
          <hr class="section-divider" />
          <ul>
            <li>ผู้ใช้งานไม่สามารถสั่งงานแอปพลิเคชัน Microsoft Office ด้วยภาษาธรรมชาติให้ทำงานซับซ้อนได้อย่างมีประสิทธิภาพและแม่นยำ</li>
          
          </ul>
        </div>
       <div class="section">
       <h2 class="section-title"> Methodology</h2>
       <hr class="section-divider" />
        <div class="sub-section">
          <h2 class="sub-section-title">พัฒนา Office Domain Specific Language (ODSL)</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>สร้างภาษาเฉพาะด้านที่มีโครงสร้างเรียบง่ายและสม่ำเสมอ เพื่อให้ LLMs สามารถเรียนรู้และแปลงคำสั่งภาษาธรรมชาติ
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">ใช้ Analysis-Retrieval Method (ARM)</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>พัฒนาเทคนิคการเลือกตัวอย่างคำสั่งและบริบทที่เกี่ยวข้องกับคำสั่งผู้ใช้โดยใช้ LLMs เพื่อสร้าง prompt ที่เหมาะสมสำหรับการแปลงคำสั่งภาษาธรรมชาติ
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">เพิ่มความแม่นยำด้วย Automatic Code Correction</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ใช้ LLMs ร่วมกับการวิเคราะห์โค้ดแบบเชิงสัญลักษณ์ เพื่อตรวจสอบข้อผิดพลาด เช่น คำสั่งไม่ถูกต้อง หรือ syntax ผิด
            </li>
          </ul>
        </div>
      </div>
      <div class="section">
        <h2 class="section-title"> Result</h2>
        <hr class="section-divider" />
        <ul>
          <li>การแปลงคำสั่งผู้ใช้เป็นโปรแกรม ODSL ได้สำเร็จในระดับความแม่นยำ 96%</li>
        
        </ul>
      </div>
      <div class="section">
        <h2 class="section-title"> Remaining problems</h2>
        <hr class="section-divider" />
        <ul>
          <li>การลดข้อผิดพลาดจากการ "hallucination" ของ LLMs และการจัดการคำสั่งที่ซับซ้อนหรือไม่สมบูรณ์ในแอปพลิเคชันเฉพาะ</li>
        
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
