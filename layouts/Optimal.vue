
  <template>
    <div class="green-layout">
      <div class="content-box">
        <h1>Optimal priority assignment for real-time systems:  a coevolution-based approach</h1>
        <div class="section">
          <h2 class="section-title"> Problem</h2>
          <hr class="section-divider" />
          <ul>
            <li>การกำหนด Priority Assignment Task-Arrival Sequence เพื่อให้ระบบเรียลไทม์สามารถจัดการงานได้อย่างมีประสิทธิภาพ โดยไม่พลาด Deadline .</li>
          
          </ul>
        </div>
       <div class="section">
       <h2 class="section-title"> Methodology</h2>
       <hr class="section-divider" />
        <div class="sub-section">
          <h2 class="sub-section-title">Initialization</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>สร้าง Solutions Priority Assignments และ Task-Arrival Sequences จากนั้นประเมิน Fitness ด้วย Safety Margins และ Deadline Misses
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">Evolution Process</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ใช้ Pareto Dominance และ Crowding Distance เพื่อเลือก Solutions ที่ดีที่สุด จากนั้นใช้ Crossover และ Mutation เพื่อสร้าง Solutions ใหม่
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">Population Update</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>เลือก Solutions ที่ดีที่สุด และใช้ Crowding Distance เพื่อรักษาความหลากหลายของ Solutions ใน Population หยุดการวิวัฒนาการเมื่อถึงจำนวนรอบที่กำหนด
            </li>
          </ul>
        </div>
    
        <div class="sub-section">
          <h2 class="sub-section-title">Solution Selection</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>เลือกคำตอบที่เหมาะสมที่สุด โดยคำนึงถึง Safety Margins และ Deadline Misses หรือความสมดุลระหว่างทั้งสอง
            </li>
          </ul>
        </div>
      </div>
      <div class="section">
        <h2 class="section-title"> Result</h2>
        <hr class="section-divider" />
        <ul>
          <li>วิธีการนี้ให้ผลลัพธ์ที่ดีกว่าการ random search และวิธีที่ใช้ในปัจจุบัน, สามารถประมวลผลได้ภายใน 16 ชั่วโมงและช่วยวิศวกรพิจารณาการแลกเปลี่ยนระหว่างระยะปลอดภัยและข้อจำกัดในการออกแบบ</li>
        
        </ul>
      </div>
      <div class="section">
        <h2 class="section-title"> Remaining problems</h2>
        <hr class="section-divider" />
        <ul>
          <li>การหาวิธีที่ดีที่สุดในการ Safety Margins เพื่อให้ระบบเสร็จทันเวลา แต่บางครั้งการเพิ่ม Safety Margins อาจทำให้ Deadline Misses เพิ่มขึ้นในขณะเดียวกัน</li>
        
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
