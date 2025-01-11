<template>
  <div class="green-layout">
    <header class="layout-header">
      <h1 class="main-title">ผลลัพธ์และประสิทธิภาพ</h1>
    </header>
    <main class="layout-content">
      <div class="section-container">
        <div class="content-section" v-for="(section, index) in sections" :key="index">
          <h3 class="section-title">{{ section.title }}</h3>
          <ul>
            <li v-for="(content, i) in section.content" :key="i">{{ content }}</li>
          </ul>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
const sections = [
  {
    title: "ผลลัพธ์จากการใช้งานจริงในแอป Alipay",
    content: [

      "Step Success Rate (Step SR): ความแม่นยำในการดำเนินงานในแต่ละขั้นตอน",
      "Task Success Rate (Task SR): ความสำเร็จในการดำเนินงานทั้งหมดให้เสร็จสมบูรณ์",
      "Baseline (AntLLM): Step SR: 52.42%, Task SR: 6.05%",
      "LLMPA Framework: Step SR: 93.71%, Task SR: 70.42%",
    ],
  },
  {
    title: "ผลลัพธ์การทดสอบมาตรฐาน (AgentBench-WB)",
    content: [
      "Step Success Rate: ความแม่นยำในการดำเนินการในแต่ละขั้นตอน",
      "Element Accuracy (Ele. Acc): ความถูกต้องในการเลือกองค์ประกอบ UI",
      "Operation F1: ความแม่นยำในการคาดการณ์คำสั่ง",
      "การใช้ Instruction Chains ช่วยเพิ่ม Step SR ในหลายโมเดล:",
      "GPT-4 with Instruction Chains: Step SR: 26.36% ",
    ],
  },
  {
    title: "การใช้งานในโลกจริง",
    content: [
      "ทดสอบในกว่า 20 สถานการณ์จริง พร้อมคำสั่งกว่า 2000 งาน",
      "มีการปรับแต่งโมเดลเป็นรายสัปดาห์เพื่อรองรับงานใหม่ ๆ",
      "การฝึกอบรม: ใช้ GPU NVIDIA A-100 จำนวน 32 ตัว",
      "การใช้งานจริง: ใช้ GPU NVIDIA A-40 จำนวน 100 ตัวใน production",
    ],
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

.main-title {
  font-size: 2rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
}

.layout-header {
  background-color: rgba(0, 0, 0, 0.8);
  width: 80%;
  padding: 15px 0;
  border-radius: 50px;
  box-shadow: 0 0 20px rgba(238, 255, 0, 0.5), 0 0 15px rgba(0, 0, 0, 0.8);
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 20px 0;
  font-size: 1rem;
  line-height: 1.5;
}

.section-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  width: 90%;
  max-width: 1200px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 15px;
  text-align: left;
}

.section-title {
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 10px;
  color: #ffba08;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

ul {
  list-style-type: disc;
  padding-left: 20px;
  font-size: 1rem;
}

li {
  margin-bottom: 5px;
  color: #f1f1f1;
}
</style>
