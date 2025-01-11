<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">วิธีการที่นำเสนอ</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Section -->
        <div class="content-section" v-for="(article, index) in articles" :key="index">
          <h3 class="section-title">{{ article.title }}</h3>
      
          <p>{{ article.publication }}</p>
   
        </div>
      </div>
    </main>


  </div>
</template>

<script setup>
const articles = [
  {
    title: "Genetic Algorithm for Optimization",
    publication: "ใช้ Genetic Algorithm ซึ่งเป็นเทคนิคการค้นหาในพื้นที่สำหรับแก้ปัญหาการเพิ่มประสิทธิภาพ ประเมินค่าความเหมาะสมของแต่ละคำตอบในประชากร เลือกคำตอบที่มีค่าความเหมาะสมสูง  Genetic Algorithm สร้างคำตอบใหม่ ทำซ้ำจนได้คำตอบที่เหมาะสมหรือดีที่สุด​",
  
  },
  {
    title: "User-Centered Interaction Design - UCID",
    publication: "ใช้ แนวคิดการออกแบบที่เน้นผู้ใช้ (Design Thinking) เพื่อสร้างระบบที่ตอบโจทย์ความต้องการของนักศึกษา​",
  },
  {
    title: "Data Engineering",
    type: "Journal",
    publication: "เพิ่มความสามารถในการจัดการข้อมูลจากรูปแบบที่หลากหลาย เช่น PDF, XML, และ HTML",
    year: "2023",
    authors: [],
  },
  {
    title: "Constraint Programming",
    type: "Journal",
    publication: "วิธีแก้ปัญหาที่ใช้ข้อกำหนดและเงื่อนไขเพื่อค้นหาคำตอบที่เหมาะสม โดยระบุตัวแปร (งาน, เวลา, ทรัพยากร) และข้อจำกัด (งานต้องเสร็จภายในกำหนดเวลา, ใช้ทรัพยากรไม่เกินที่มีอยู่) พร้อมทั้งตั้งเป้าหมาย​",
    year: "ฤดูร้อน 2007",
    authors: [
      "Karen Myers",
      "Pauline Berry",
      "Jim Blythe",
      "Ken Conley",
      "Melinda Gervasio",
      "Deborah McGuinness",
      "David Morley",
      "Avi Pfeffer",
      "Martha Pollack",
      "Milind Tambe",
    ],
  }
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
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 10px;
  width: 90%;
  max-width: 1000px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 10px;
  text-align: left;
  display: flex;
  flex-direction: column;
  font-size: 0.85rem; /* ลดขนาดตัวอักษรภายในกล่อง */
}

.section-title {
  font-size: 1.0rem;
  font-weight: bold;
  margin-bottom: 3px;
  color: #eae213; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5); /* เพิ่มเงาให้ตัวอักษร */
  font-weight: bold; /* เน้นความหนา */
}
.content-section p strong {
  color: #ffba08; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  font-size: 0.9rem; /* ปรับขนาดตัวอักษร */
 
}

</style>
