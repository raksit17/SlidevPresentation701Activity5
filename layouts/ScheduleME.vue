<template>
    <div class="activity-layout">
      <!-- Section 1 ทำหน้าที่เหมือน br -->
      <div class="section1"></div>
      <br><br>
      <br><br>
      <!-- Section หลัก -->
      <div class="section">
        <motion :initial="{ opacity: 0, y: -20 }" :animate="{ opacity: 1, y: 0 }" transition="0.8s">
          <h1 class="main-title">A Smart Personal AI Assistant for Visually Impaired People</h1>
        </motion>
      </div>
    
      <!-- Content Box -->

    </div>
  </template>
  
  <style scoped>
  /* Activity Layout */
  .activity-layout {
    background-image: url('/assets/images/4.1.1.jpg');
    background-color: rgba(0, 0, 0, 0.6); /* เพิ่มความเข้มของ overlay */
    background-size: cover;
    background-position: center;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  /* Section1: ใช้แทน br */
  .section1 {
    height: 90px; /* ปรับความสูงตามที่ต้องการ */
    width: 100%;
    background-color: transparent;
  }
  
  /* Section */
  .section {
    margin-bottom: 10px;
    background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent box */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.9);
    width: 100%;
    padding: 5px;
    border-radius: 10px;
    display: flex;
    justify-content: center; /* จัดให้อยู่กึ่งกลางแนวนอน */
    align-items: center; /* จัดให้อยู่กึ่งกลางแนวตั้ง */
    min-height: 150px; /* กำหนดความสูงขั้นต่ำเพื่อให้มีพื้นที่จัดกึ่งกลาง */
  }
  
  /* Main Title */
  .main-title {
    color: #f1f1f1; /* สีขาวอ่อนเพื่อให้มองเห็นง่าย */
    font-size: 3rem;
    margin-bottom: 0; /* ลบ margin ด้านล่างเพื่อจัดให้อยู่กึ่งกลาง */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8); /* เพิ่มความชัดเจนด้วย shadow */
    text-align: center; /* จัดข้อความให้อยู่กึ่งกลางภายใน */
  }
  
  
  /* Content Box */
  .content-box {
    width: 90%;
    text-align: center;
    padding: 30px;
    border: 3px solid #ccc; /* ใช้สีเทาอ่อนเพื่อไม่ให้ตัดกับพื้นหลังมากเกินไป */
    border-radius: 15px;
    background-color: rgba(0, 0, 0, 0.8); /* Semi-transparent box */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    overflow-y: auto;
    max-height: 90vh;
  }
  
  /* Description Title */
  .description-title {
    color: #e0e0e0; /* ใช้สีอ่อนที่ยังคงความชัดเจน */
    font-size: 1.8rem;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6); /* เพิ่มความชัดเจนของข้อความ */
  }
  
  /* Highlight Content */
  .highlight-content {
    color: #ffcc00; /* สีเหลืองทองที่สว่างและเข้ากับพื้นหลัง */
  }
  </style>
  