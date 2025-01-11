<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">เอกสาร</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Section -->
        <div class="content-section" v-for="(article, index) in articles" :key="index">
          <h3 class="section-title">{{ article.title }}</h3>
       
            <a :href="article.type" target="_blank" rel="noopener noreferrer">{{ article.type }}</a>
         
          

      </div>
      </div>
    </main>


  </div>
</template>

<script setup>
const articles = [
  {
    title: "Natural Language Commanding via Program Synthesis",
    type: "https://drive.google.com/file/d/1kLm8GpmuS22UnxMRYAUVPHfk4cbZ8Wcr/view?usp=sharing",
  },
  {
    title: "Optimal Priority Assignment for Real-Time Systems: A Coevolution-Based Approach",
    type: "https://drive.google.com/file/d/1fS9bqUrISscJs0d7iUek9OHusAw-hZpQ/view?usp=sharing",
 

  },
  {
    title: "TaDeR: A New Task Dependency Recommendation for Project Management Platform",
    type: "https://drive.google.com/file/d/1hun-38Rl1ZVMv1N66konmm3CRCBYXoHb/view?usp=sharing",

  },
  {
    title: "Task Management System Using AI Prioritizations",
    type: "https://drive.google.com/file/d/1jQgAF-kOw380PRux14edIfn2RN9geUN_/view?usp=sharing",
    
  },
  {
    title: "NL2CMD: An Updated Workflow for Natural Language to Bash Commands Translation",
    type: "https://drive.google.com/file/d/1pAqT7nPic1v2Jf0qenDHW5u3seXJ4U41/view?usp=sharing",
  
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
  font-size: 0.85rem; /* ลดขนาดตัวอักษรภายในกล่อง */
  overflow: hidden; /* ซ่อนข้อความที่เกินออกมา */
  word-wrap: break-word; /* ตัดคำหากข้อความยาวเกิน */
}
a {
  white-space: nowrap; /* ไม่ตัดบรรทัด */
  overflow: hidden; /* ซ่อนข้อความที่เกิน */
  text-overflow: ellipsis; /* แสดง ... หากข้อความยาวเกิน */
  display: block; /* ทำให้ลิงก์จัดตำแหน่งในกล่องได้ดีขึ้น */
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
