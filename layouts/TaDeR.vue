
  <template>
    <div class="green-layout">
      <div class="content-box">
        <h1>TaDeR: A New Task Dependency Recommendation</h1>
        <div class="section">
          <h2 class="section-title"> Problem</h2>
          <hr class="section-divider" />
          <ul>
            <li>การค้นหาและเชื่อมโยงงานใหม่กับงานเดิมในโปรเจกต์ในซอฟต์แวร์ที่มีจำนวนงานมากเป็นงานที่ใช้เวลาและความพยายามมาก</li>
          
          </ul>
        </div>
       <div class="section">
       <h2 class="section-title"> Methodology</h2>
       <hr class="section-divider" />
        <div class="sub-section">
          <h2 class="sub-section-title">Data Processing</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>จัดการข้อมูลข้อความ ลบ Noise จัดการ NaN data แปลงเป็น Root Form (Stemming) เลือกคุณสมบัติสำคัญ เช่น Title, Description, Summary
            </li>
            <li>
              <span class="icon">☘️</span>การสร้างฟีเจอร์ใหม่เน้นการเพิ่มข้อมูลเชิงเวลาและบริบทข้อความ เช่น ความแตกต่างของวันที่ การรวมข้อความ และการกรองงานตามช่วงเวลา เพื่อปรับปรุงความแม่นยำของโมเดล.
            </li>
        
          </ul>
        </div>
        <div class="sub-section">
          <h2 class="sub-section-title">Modeling</h2>
          <ul>
            <li>
              <span class="icon">☘️</span>Embedding Layer (GloVe หรือ FastText) สำหรับแปลงข้อความเป็นเวกเตอร์เชิงตัวเลข
            </li>
            <li>
              <span class="icon">☘️</span>CNN โดยดึงคุณสมบัติที่สำคัญ จาก Embedding Layer ใช้ Convolutional Filters เพื่อตรวจจับรูปแบบในข้อมูล เช่น คำที่สัมพันธ์กันในบริบท
            </li>
            <li>
              <span class="icon">☘️</span>Dense Layer คำนวณคะแนนความสัมพันธ์ระหว่างข้อความสองชุด รับผลลัพธ์จาก CNN มาและประมวลผลเพื่อตัดสินความสัมพันธ์
            </li>
              
           
          </ul>
        </div>
      </div>
      <div class="section">
        <h2 class="section-title"> Result</h2>
        <hr class="section-divider" />
        <ul>
          <li>โมเดล GloVe + CNN พร้อม Time Filter 1 เดือน ใช้ได้ดีในระดับหนึ่ง แต่ยังมีช่องว่างให้ปรับปรุง เนื่องจากค่า Accuracy@1 และ MRR@1 ที่ 0.2335 ถือว่ายังไม่สูงมากนัก</li>
        
        </ul>
      </div>
      <div class="section">
        <h2 class="section-title"> Remaining problems</h2>
        <hr class="section-divider" />
        <ul>
          <li>โมเดลยังขาดความแม่นยำสูง ไม่รองรับความสัมพันธ์ระหว่างงาน และมีข้อจำกัดด้านการใช้งานในโลกจริงและทรัพยากร</li>
        
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
