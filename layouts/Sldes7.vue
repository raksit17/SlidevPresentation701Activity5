<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">ข้อสรุปและข้อมูลที่ได้จากการศึกษา</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Objective Section -->
        <div class="content-section">
          <h2 class="section-header">กลุ่มบทความ</h2>
          <ul class="list-items">
            <li>
              <strong>การจัดตารางเวลาและการจัดสรรทรัพยากรที่มีประสิทธิภาพ:</strong>
              พัฒนาระบบ AI-powered timeline scheduler
            </li>
            <li>
              <strong>การปรับตัวและการปรับปรุงอย่างต่อเนื่อง:</strong>
              สามารถปรับตัวตามสถานการณ์ที่เปลี่ยนแปลงได้
            </li>
            <li>
              <strong>ความพึงพอใจของผู้ใช้และฟีเจอร์ที่ใช้งานง่าย:</strong>
              เน้นการพัฒนาฟีเจอร์ที่เข้าใจง่ายและตอบโจทย์ความต้องการของผู้ใช้
            </li>
          </ul>
        </div>

        <!-- Scope Section -->
        <div class="content-section">
          <h2 class="section-header">ขอบเขตของการวิจัย</h2>
          <ul class="list-items">
            <li>
              <strong>การแก้ไขข้อจำกัดของเครื่องมือดั้งเดิม:</strong>
              ใช้อัลกอริธึมขั้นสูงและการเรียนรู้ของเครื่องเพื่อเพิ่มประสิทธิภาพ
            </li>
            <li>
              <strong>การเพิ่มประสิทธิภาพและการจัดการเวลา:</strong>
               ระบบนี้มีเป้าหมายที่จะเปลี่ยนแปลงวิธีการที่บุคคลและทีมงานจัดการเวลาของพวกเขา 
            </li>
            <li>
              <strong>การจัดตารางเวลาที่ปรับเปลี่ยนได้และเป็นส่วนตัว:</strong>
              เรียนรู้จากพฤติกรรมของผู้ใช้เพื่อปรับกระบวนการจัดตารางเวลาอย่างต่อเนื่อง
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
