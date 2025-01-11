<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">สรุป</h1>
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
          <p>{{ section.key }}</p>
          <p>{{ section.relevance }}</p>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <footer class="layout-footer">
      <p>© 2024 AI Scheduler Presentation</p>
    </footer>
  </div>
</template>

<script setup>
const sections = [
 {
    title: "การแปลงภาษาธรรมชาติเป็นคำสั่งที่สามารถทำงานได้:",
    key: "Semantic parsing และโปรแกรม synthesis สามารถแปลงข้อความธรรมชาติเป็นคำสั่งที่ระบบเข้าใจได้อย่างแม่นยำ",
    relevance: "สนับสนุน Message Processing Module ในการแปลงข้อความจาก LINE ให้เป็นคำสั่งที่ระบบสามารถประมวลผลได้"
  },
  {
    title: "การจัดลำดับความสำคัญของงานแบบเรียลไทม์:",
    key: "การใช้เทคนิค Rate-Monotonic Scheduling ช่วยจัดลำดับงานโดยอิงจากความเร่งด่วนและ Deadline",
    relevance: "ช่วย AI Prioritization Module จัดการลำดับความสำคัญของงานตามข้อมูลเช่น Deadline และ Impact แบบเรียลไทม์"
  },
  {
    title: "การแนะนำและจัดการความสัมพันธ์ของงาน:",
    key: "CNN และ embedding เช่น GloVe มีประสิทธิภาพในการวิเคราะห์และแนะนำความสัมพันธ์ระหว่างงาน",
    relevance: "เพิ่มประสิทธิภาพ Task Management Module โดยแนะนำความสัมพันธ์ระหว่างงานและปรับปรุงการทำงานของ Workflow"
  }
];

</script>

<style scoped>
.green-layout {
  background-image: url('/assets/images/pexels-brandandpalms-768938.jpg');
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
  max-width: 1200px;
  padding: 20px 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 20px;
  text-align: left;
  font-size: 0.9rem;
}

.section-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #cdc845;
  margin-bottom: 10px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.layout-footer {
  font-size: 0.85rem;
  color: #f1f1f1;
  text-align: center;
}
</style>