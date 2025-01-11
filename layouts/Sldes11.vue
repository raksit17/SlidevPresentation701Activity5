<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">ปัญหาที่ยังคงเหลืออยู่</h1>
    </header>


    <main class="layout-content">
      <div class="section-container">

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
    title: "คุณภาพและปริมาณของข้อมูล",
    content:
      "ความแม่นยำของระบบจัดตารางเวลาขึ้นอยู่กับคุณภาพและปริมาณของข้อมูลที่ระบบได้รับ ข้อมูลที่ไม่ดีสามารถนำไปสู่การจัดตารางเวลาและการจัดสรรทรัพยากรที่ไม่เหมาะสม ซึ่งจะส่งผลกระทบต่อประสิทธิภาพโดยรวมของระบบ​​",
  },
  {
    title: "การต่อต้านจากผู้ใช้",
    content:
      "อาจมีความเสี่ยงที่ผู้ใช้จะต่อต้านการใช้งานระบบที่ขับเคลื่อนด้วย AI เนื่องจากขาดความไว้วางใจในระบบอัตโนมัติ ผู้ใช้บางคนอาจชอบควบคุมตารางเวลาของตนเองด้วยมือ ซึ่งอาจทำให้การนำระบบ AI ไปใช้ยากขึ้น​​"
  },
  {
    title: "ข้อกังวลด้านความเป็นส่วนตัวและความปลอดภัย",
    content:
      "การจัดการข้อมูลที่ละเอียดอ่อนเกี่ยวกับการจัดตารางเวลาและทรัพยากรอาจทำให้เกิดข้อกังวลเกี่ยวกับความเป็นส่วนตัวและความปลอดภัย ต้องมีการจัดการเรื่องเหล่านี้อย่างเข้มงวดเพื่อป้องกันการรั่วไหลของข้อมูลและสร้างความเชื่อมั่นให้กับผู้ใช้​​"
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
