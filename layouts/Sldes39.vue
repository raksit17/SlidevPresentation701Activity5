<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">เป้าหมาย วัตถุประสงค์ ขอบเขต</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Objective Section -->
        <div class="content-section">
          <h2 class="section-header">เป้าหมายและวัตถุประสงค์ของการวิจัย</h2>
          <ul class="list-items">
            <li>
              <strong>พัฒนาวิธีการแสดงผล UI ที่เน้นฟังก์ชันการทำงาน</strong>
              สร้างวิธีการแปลงส่วนต่อประสานผู้ใช้ (UI) ให้อยู่ในรูปแบบข้อความที่ LLMs สามารถเข้าใจได้
            </li>
            <li>
              <strong>เสริมความรู้เฉพาะทางให้กับ LLMs</strong>
              เพิ่มพูนความรู้เฉพาะด้านเกี่ยวกับแอปพลิเคชันให้กับ LLMs ผ่านการวิเคราะห์แอปพลิเคชันและเทคนิคการเพิ่มหน่วยความจำ
            </li>
            <li>
              <strong>ปรับปรุงต้นทุนการประมวลผลของโมเดล</strong>
              ลดต้นทุนและความซับซ้อนในการประมวลผลข้อมูลของ LLMs ด้วยการปรับแต่งกระบวนการเรียกใช้โมเดล
            </li>
          </ul>
        </div>

        <!-- Scope Section -->
        <div class="content-section">
          <h2 class="section-header">ขอบเขตของการวิจัย</h2>
          <ul class="list-items">
            <li>
              <strong>เป้าหมาแอปพลิเคชัน</strong>
              AutoDroid ถูกออกแบบมาเพื่อทำงานอัตโนมัติในแอป Android หลากหลาย รวมถึงแอปที่ไม่มี API หรือการสนับสนุนจากนักพัฒนา
            </li>
            <li>
              <strong>การผสานเทคโนโลยี:</strong>
              ระบบรวม LLMs เช่น GPT-3.5, GPT-4, และ Vicuna-7B พร้อมเทคนิคขั้นสูงในการวิเคราะห์ UI และสร้างงาน 
            </li>
            <li>
              <strong>การทดสอบและเกณฑ์มาตรฐาน:</strong>
              งานวิจัยพัฒนาเกณฑ์มาตรฐาน (DroidTask) ที่มี 158 งาน เพื่อประเมินประสิทธิภาพในสถานการณ์ที่หลากหลาย
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
  padding: 10px 0;
}

.section-container {
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 100%;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 10px;
  text-align: left;
  font-size: 1rem;
  
}

.section-header {
  font-size: 1.5rem;
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
