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
          <p><strong>ประเภทบทความ:</strong> {{ article.type }}</p>
          <p><strong>ชื่อสิ่งตีพิมพ์:</strong> {{ article.publication }}</p>
          <p><strong>ปีที่ตีพิมพ์:</strong> {{ article.year }}</p>
          <p>
            <strong>ผู้เขียน:</strong>
            <span v-if="article.authors.length">{{ article.authors.join(', ') }}</span>
            <span v-else>ไม่มีการระบุชื่อผู้เขียน</span>
          </p>
          <p><strong>สรุป:</strong> {{ article.summary }}</p>
        </div>
      </div>
    </main>


  </div>
</template>


<script setup> 
const articles = [
  {
    title: "Natural Language Commanding via Program Synthesis",
    type: "Journal Article",
    publication: "Microsoft Research",
    year: "2023",
    authors: ["Apurva Gandhi", "Thong Q. Nguyen", "Huitian Jiao", "Robert Steen", "Ameya Bhatawdekar"],
    summary: "ระบบ AI ที่สามารถแปลคำสั่งจากภาษาธรรมชาติให้สามารถทำงานกับแอปพลิเคชันต่าง  เช่น Microsoft Office"
  },
  {
    title: "Optimal Priority Assignment for Real-Time Systems: A Coevolution-Based Approach",
    type: "Journal Article",
    publication: "Empirical Software Engineering",
    year: "2022",
    authors: ["Jaekwon Lee", "Seung Yeob Shin", "Shiva Nejati", "Lionel C. Briand"],
    summary: "วิธีการตั้งค่าลำดับความสำคัญในระบบ Realtime โดยใช้กระบวนการ Coevolution ซึ่งช่วยเพิ่มประสิทธิภาพและความยืดหยุ่นในระบบที่ต้องการจัดการงานภายใต้ข้อจำกัดทางเวลา."
  },
  {
    title: "TaDeR: A New Task Dependency Recommendation for Project Management Platform",
    type: "Journal Article",
    publication: "Applied Intelligence",
    year: "2022",
    authors: ["Quynh Nguyen", "Dac H. Nguyen", "Son T. Huynh", "Hoa K. Dam", "Binh T. Nguyen"],
    summary: "บทความนี้นำเสนอระบบ (TaDeR) สำหรับแพลตฟอร์มการจัดการโครงการ โดยใช้เทคนิคการเรียนรู้เชิงลึกเพื่อแนะนำงานที่เกี่ยวข้องกับงานใหม่."
  },
  {
    title: "Task Management System Using AI Prioritizations",
    type: "Journal Article",
    publication: "International Journal of Engineering Research & Technology",
    year: "2024",
    authors: ["Manazir Musthafa", "Dr. Amj Muthukumaran"],
    summary: "บทความนี้นำเสนอระบบการจัดการงานโดยใช้ AI เพื่อช่วยในการตั้งลำดับความสำคัญของงาน"
  },
  {
    title: "NL2CMD: An Updated Workflow for Natural Language to Bash Commands Translation",
    type: "Journal Article",
    publication: "River Journal",
    year: "2023",
    authors: ["Quchen Fu", "Zhongwei Teng", "Marco Georgaklis", "Jules White", "Douglas C. Schmidt"],
    summary: "วิจัยที่สร้างโมเดลที่ใช้ในการแปลคำสั่ง Bash จากภาษาธรรมชาติ ."
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
