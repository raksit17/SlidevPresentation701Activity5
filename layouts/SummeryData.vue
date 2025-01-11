<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">รายการบทความวิชาการ</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Section -->
        <div class="content-section" v-for="(article, index) in articles" :key="index">
          <h3 class="section-title">{{ article.title }}</h3>
          <p><strong>วิธีการ:</strong> {{ article.method }}</p>
          <p><strong>เทคนิค:</strong> {{ article.technique }}</p>
        </div>
      </div>
    </main>


  </div>
</template>



<script setup> 
const articles = [ 
  {
    title: "TaDeR: A New Task Dependency Recommendation for Project Management Platform",
    method: "ใช้ Deep Neural Networks สำหรับการแนะนำความสัมพันธ์ระหว่างงาน โดยใช้ GloVe embedding และ CNN ในการสกัดคุณลักษณะและฝึกโมเดล",
    technique: "Siamese networks, GRU, CNN, LSTM, TF-IDF และการใช้ cosine similarity กับ Euclidean distance"
  },
  {
    title: "Task Management System Using AI Prioritizations",
    method: "ใช้ AI สำหรับการจัดลำดับความสำคัญของงาน โดยใช้ Machine Learning เพื่อพิจารณาประวัติข้อมูลและการกำหนดลำดับความสำคัญ",
    technique: "Random Forest สำหรับการคาดการณ์ลำดับความสำคัญ และ Linear Regression สำหรับการทำนายกำหนดเวลา"
  },
  {
    title: "NL2CMD: An Updated Workflow for Natural Language to Bash Commands Translation",
    method: "ใช้ Transformer models สำหรับการแปลคำสั่งจากภาษาธรรมชาติเป็นคำสั่ง Bash โดยใช้ชุดข้อมูล NL2CMD ที่มีขนาดใหญ่และไม่พึ่งพาคำสั่ง Bash ที่มีอยู่แล้ว",
    technique: "Back-translation, Data augmentation, Transformer models สำหรับการแปลคำสั่ง"
  },
  {
    title: "Optimal Priority Assignment for Real-Time Systems",
    method: "ใช้ Multi-objective Competitive Coevolutionary Algorithms เพื่อหาวิธีการจัดลำดับความสำคัญในระบบเรียลไทม์ โดยจำลองการโต้ตอบระหว่างทีมพัฒนาและทีมทดสอบในการหาโซลูชันที่ดีที่สุด",
    technique: "Coevolutionary algorithms, Multi objective optimization สำหรับการค้นหาคำตอบที่ดีที่สุด"
  },
  {
    title: "Natural Language Commanding via Program Synthesis",
    method: "ใช้ Semantic Interpreter โดยใช้ LLMs เพื่อแปลคำสั่งภาษาธรรมชาติให้เป็นโปรแกรมที่สามารถทำงานในแอปพลิเคชันต่างๆ เช่น Microsoft Office โดยใช้ Office Domain Specific Language (ODSL)",
    technique: "LLMs,Analysis-Retrieval Prompt Construction (ARM), Retrieval augmented generation (RAG)"
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
.main-title {
  font-size: 1.5rem;
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

.gradient-title {
  font-size: 1.5rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
  margin: 0;
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 20px 0;
  font-size: 1rem; /* ปรับขนาดตัวอักษรสำหรับเนื้อหาทั้งหมด */
  line-height: 1.5; /* เพิ่มระยะห่างระหว่างบรรทัด */
}

.section-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 10px;
  width: 90%;
  max-width: 1000px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 6px;
  text-align: left;
  display: flex;
  flex-direction: column;
  font-size: 0.8rem; /* ลดขนาดตัวอักษรภายในกล่อง */
}

.section-title {
  font-size: 0.8rem;
  font-weight: bold;
  margin-bottom: 3px;
  color: #eae213; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5); /* เพิ่มเงาให้ตัวอักษร */
  font-weight: bold; /* เน้นความหนา */
}
.content-section p strong {
  color: #ffba08; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  font-size: 0.8rem; /* ปรับขนาดตัวอักษร */
 
}

</style>
