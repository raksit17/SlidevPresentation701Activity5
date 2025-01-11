<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">ผลกระทบของปัญหา</h1>
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

    <!-- Footer -->
    <footer class="layout-footer">
      <p>© 2024 AI Scheduler Presentation</p>
    </footer>
  </div>
</template>

<script setup>
const sections = [
  {
    title: "การขยายตัวและประสิทธิภาพ",
    content:
      "หากปรับปรุงด้านนี้ จะช่วยให้แอปพลิเคชันมือถือใช้งานง่ายขึ้นและรองรับงานหลากหลายได้โดยไม่ต้องตั้งค่าด้วยตนเองมากนัก",
  },
  {
    title: "ประสบการณ์ของผู้ใช้ ",
    content:
      "ความยุ่งยากจากการใช้แรงงานคนในระบบปัจจุบันเป็นอุปสรรคต่อการทำงานอัตโนมัติที่มีประสิทธิภาพ",
  },
  {
    title: "ต้นทุนและการใช้ทรัพยากร",
    content:
      "การปรับแต่งกระบวนการสอบถามและการสร้างงานช่วยลดภาระการประมวลผล ทำให้สามารถทำงานได้อย่างมีประสิทธิภาพ",
  },
];
</script>

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