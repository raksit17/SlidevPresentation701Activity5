<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">วิธีการนำเสนอ</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Objective Section -->
        <div class="content-section">
          <h2 class="section-header">LLM-Based Process Automation</h2>
          <ul class="list-items">
            <li>
              <strong>Instruction Chains Generator</strong>
              แยกคำสั่งซับซ้อนออกเป็นขั้นตอนย่อยที่ชัดเจน
            </li>
            <li>
              <strong>Previous Action Description Generator</strong>
              สรุปการกระทำก่อนหน้าและเชื่อมโยงบริบทของหน้าแอป
            </li>
            <li>
              <strong>Object Detection Module:</strong>
              ใช้โมเดล YOLOX ในการวิเคราะห์ตรวจจับองค์ประกอบ UI ในหน้าแอป เช่น ปุ่มและช่องกรอกข้อมูล
            </li>
            <li>
              <strong>Action Prediction Module:</strong>
              ทำนายการกระทำถัดไปที่จำเป็น
            </li>
            <li>
              <strong>Controllable Calibration Module</strong>
              ตรวจสอบความสมเหตุสมผลของลำดับการกระทำ
            </li>
          </ul>
        </div>

        <!-- Scope Section -->
        <div class="content-section">
          <h2 class="section-header">กระบวนการทำงานของ LLMPA</h2>
          <ul class="list-items">
            <li>
              <strong>รับอินพุต:</strong>
              ผู้ใช้ระบุคำขอ เช่น "ช่วยจองตั๋วเครื่องบินจากกรุงเทพไปเชียงใหม่ วันที่ 15 มกราคม"
            </li>
            <li>
              <strong>สร้างคำสั่ง:</strong>
              ระบบสร้างคำสั่งเป็นขั้นตอนย่อยที่เข้าใจได้
            </li>
            <li>
              <strong>ดำเนินการ:</strong>
              ระบบระบุองค์ประกอบในแอป เช่น ปุ่มหรือช่องข้อมูล และดำเนินการคำสั่งทีละขั้นตอน
            </li>
            <li>
              <strong>การปรับเทียบ:</strong>
              ตรวจสอบความถูกต้องของคำสั่งและปรับปรุงลำดับการดำเนินการ
            </li>
            <li>
              <strong>เสร็จสิ้น</strong>
               ดำเนินงานจนเสร็จสมบูรณ์
            </li>
          </ul>
        </div>
      </div>
    </main>



  </div>
</template>

<style scoped>
.green-layout {
  background-image: url('/assets/images/4.1.3.jpg');
  background-size: cover;
  background-position: center;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}

.layout-header {
  background-color: rgba(0, 0, 0, 0.8);
  width: 80%;
  padding: 15px 0;
  border-radius: 50px;
  box-shadow: 0 0 20px rgba(211, 225, 8, 0.5), 0 0 15px rgba(0, 0, 0, 0.8);
}

.main-title {
  font-size: 2rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 90%;
  max-width: 1000px;
  padding: 5px 0;
}

.section-container {
  display: flex;
  flex-direction: column;
  gap: 3px;
  width: 100%;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 6px;
  text-align: left;
  font-size: 0.9rem;
  
}

.section-header {
  font-size: 1.0rem;
  font-weight: bold;
  color: #cdc845;
  margin-bottom: 10px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.list-items {
  list-style: none;
  padding: 0;
}

.list-items li {
  margin-bottom: 15px;
}

.list-items strong {
  color: #ffba08;
  font-weight: bold;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.layout-footer {
  font-size: 0.85rem;
  color: #f1f1f1;
  text-align: center;
}
</style>
