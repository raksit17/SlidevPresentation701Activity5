
  <template>
    <div class="green-layout">
      <div class="content-box">
        <h1>Task Management System Using AI Prioritizations</h1>
        <div class="section">
          <h2 class="section-title"> Problem</h2>
          <hr class="section-divider" />
          <ul>
            <li>ระบบยังขาดความแม่นยำและความยืดหยุ่นในการจัดลำดับงานในสถานการณ์ซับซ้อนและสำหรับผู้ใช้ใหม่ที่มีข้อมูลจำกัด</li>
          
          </ul>
        </div>
       <div class="section">
       <h2 class="section-title"> Methodology</h2>
       <hr class="section-divider" />
        <div class="sub-section">
          <h2 class="sub-section-title">Data Processing</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>สร้างคุณลักษณะสำคัญจากข้อมูล เช่น ความสำคัญของงาน, ระดับความเร่งด่วน, และข้อเสนอแนะจากผู้ใช้ แปลงข้อมูล ให้เป็นตัวเลข เพื่อให้โมเดล AI สามารถนำไปใช้งานได้
            </li>
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">Modeling</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>ใช้ Random Forest สำหรับการคาดการณ์ลำดับความสำคัญของงาน โดยพิจารณาปัจจัยต่างๆ เช่น กำหนดส่งและความเร่งด่วน
            </li>
            <li>
              <span class="icon">☘️</span>ใช้ K-Nearest Neighbors (KNN) เพื่อการแนะนำงานแบบ Collaborative Filtering โดยระบุผู้ใช้ที่มีลักษณะการจัดการงานคล้ายกัน
            </li>
            <li>
              <span class="icon">☘️</span>ใช้ Linear Regression สำหรับการประเมินเวลาส่งงานและความต้องการของทรัพยากร
            </li>
              
           
          </ul>
        </div>
      </div>
      <div class="section">
        <h2 class="section-title"> Result</h2>
        <hr class="section-divider" />
        <ul>
          <li>Random Forest มีความแม่นยำสูงสุดที่ 92% รองลงมาคือ KNN 85% ซึ่งเน้นการปรับตัวตามผู้ใช้ และ Linear Regression 75% เหมาะกับความสัมพันธ์เชิงเส้น</li>
        
        </ul>
      </div>
      <div class="section">
        <h2 class="section-title"> Remaining problems</h2>
        <hr class="section-divider" />
        <ul>
          <li>ระบบยังขาดความยืดหยุ่นสำหรับผู้ใช้ใหม่ที่มีข้อมูลจำกัดและการจัดการงานในสถานการณ์ซับซ้อน รวมถึงต้องการความโปร่งใสเพิ่มเติมในการตัดสินใจของ AI เพื่อเพิ่มความเชื่อมั่นของผู้ใช้</li>
        
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
