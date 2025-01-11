<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">AI-Powered Task Prioritization with LINE Integration</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="grid-container">
        <!-- Sections -->
        <div
          class="content-section"
          v-for="(section, index) in sections"
          :key="index"
        >
          <h3 class="section-title">{{ section.title }}</h3>
          <p>{{ section.content }}</p>
        </div>
      </div>
    </main>

  </div>
</template>

<script setup>
const sections = [
  {
    title: "การจัดลำดับความสำคัญของงานที่ไม่ชัดเจน",
    content:
      "ทีมงานหรือผู้ใช้งานมักประสบปัญหาในการตัดสินใจว่าควรทำงานใดก่อน เนื่องจากไม่มีระบบจัดลำดับความสำคัญ  ",
  },
  {
    title: "การรับมือกับ Interrupt และการเปลี่ยนลำดับงาน",
    content:
      "งานใหม่หรือปัญหาเร่งด่วน (Interrupt) ที่เข้ามากะทันหัน เช่น Bug สำคัญ มักทำให้การจัดลำดับงานเดิมเสียหาย",
  },
  {
    title: "การวิเคราะห์ประสิทธิภาพของทีมในระยะยาว",
    content:
      "ระบบมักเน้นการวิเคราะห์งานในระยะสั้น เช่น สถานะงานหรือการจัดลำดับความสำคัญ แต่ไม่มีการวิเคราะห์เชิงลึกในระยะยาวเกี่ยวกับประสิทธิภาพของทีม",
  },

];
</script>
<style scoped>
.green-layout {
  background-image: url('/assets/images/pexels-brandandpalms-768938.jpg');
  background-size: cover;
  background-position: center;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  height: 100vh;
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
  justify-content:  space-between; /* กึ่งกลางแนวนอน */
  width: 90%;
  max-width: 1000px;
  padding: 20px 0;
}

.section-container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 16px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 1.0);
  padding: 13px;
  text-align: left;
  font-size: 1.0rem;
}

.section-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #ffba08;
  margin-bottom: 10px;
}

.layout-footer {
  font-size: 0.85rem;
  color: #f1f1f1;
  text-align: center;
}
</style>

