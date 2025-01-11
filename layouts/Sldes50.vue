<template>
  <div class="green-layout">
    <header class="layout-header">
      <h1 class="main-title">สรุปแต่ล่ะเอกสาร</h1>
    </header>
    <main class="layout-content">
      <div class="grid-container">
        <div class="grid-item" v-for="(article, index) in articles" :key="index">
          <h3 class="item-title">{{ article.title }}</h3>
          <ul>
            <li v-for="(feature, i) in article.features" :key="i">{{ feature }}</li>
          </ul>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
const articles = [
  {
    title: "An Intelligent Personal  Assistant for Task and  Time Management",
    features: [
      "ระบบ PExA เป็นระบบที่ใช้ AI ในการช่วยเหลือการจัดการงานและเวลาสำหรับผู้ใช้งานในองค์กร",
      "การจัดการงานและเวลาในระบบเดียว",
      "ความสามารถในการปรับตัวตามพฤติกรรมของผู้ใช้",
    ],
  },
  {
    title: "AutoDroid: LLM-powered Task Automation in Android",
    features: [
      "AutoDroid ใช้ (LLMs) เพื่อดำเนินการงานต่าง บนแอปพลิเคชัน Android",
      "การแปลง GUI ให้เป็นตัวแทนสำหรับการดำเนินการงาน",
      "การวิเคราะห์แอปพลิเคชันแบบไดนามิกเพื่อสร้างความรู้เฉพาะโดเมน",
  
    ],
  },
  {
    title: "Intelligent Virtual Assistants with LLM-based Process Automation",
    features: [
      "ระบบนี้ใช้ LLM ในการช่วยอัตโนมัติสำหรับงานส่วนตัวและงานในองค์กร",
      "การปรับแต่งตามความต้องการของผู้ใช้",
      "การผสานรวม LLM กับเครื่องมือและกระบวนการทำงานที่มีอยู่",
      "ความยืดหยุ่นสูงสำหรับการใช้งานที่หลากหลาย",
    ],
  },
  {
    title: "Time Line Scheduler Using AI",
    features: [
      "การจัดลำดับความสำคัญของงานด้วย AI",
      "การแก้ไขปัญหาการชนกันของตารางเวลา",
      "ใช้ข้อมูลในอดีตเพื่อทำนายและป้องกันปัญหาในอนาคต",
    ],
  },
  {
    title: "A Smart Personal AI Assistant for Visually Impaired People",
    features: [
      "ผู้ช่วยอัจฉริยะที่ช่วยผู้ใช้งานจัดการงานประจำวัน",
      "ออกแบบโดยคำนึงถึงผู้ใช้เป็นศูนย์กลางเพื่อการจัดการงานที่ใช้งานง่าย",
      "อัลกอริทึมที่ซับซ้อนสำหรับการจัดลำดับความสำคัญของงาน",
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
  width: 100%;
  padding: 20px 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 5px;
  width: 90%;
  max-width: 1200px;
}

.grid-item {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 8px;
  text-align: left;
}

.item-title {
  font-size: 0.9rem;
  font-weight: bold;
  color: #ffba08;
  margin-bottom: 10px;
}

ul {
  list-style-type: disc;
  padding-left: 20px;
}

li {
  margin-bottom: 5px;
  font-size: 0.8rem;
}
</style>
