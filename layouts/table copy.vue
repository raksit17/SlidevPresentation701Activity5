<template>
  <div class="green-layout">
    <header class="layout-header">
      <h1 class="main-title">ประเภทงาน</h1>

    </header>

    <main class="layout-content">
      <div class="content-section">
        <h2 class="section-title">ประเภทงาน</h2>
        <table>
          <thead>
            <tr>
              <th>ประเภท</th>
              <th>Feature</th>
              <th>Bug</th>
              <th>Maintenance</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>โปรเจคใหม่</td>
              <td>- พัฒนาฟีเจอร์พื้นฐานของระบบ</td>
              <td>- แก้ไขข้อผิดพลาดระหว่างพัฒนา</td>
              <td>- ปรับปรุงโครงสร้างระบบสำหรับใช้งานในอนาคต</td>
            </tr>
            <tr>
              <td>โปรเจคเก่า</td>
              <td>- เพิ่มฟีเจอร์ใหม่ในระบบเดิม</td>
              <td>- แก้ไขข้อผิดพลาดในระบบที่ใช้งานอยู่แล้ว</td>
              <td>- บำรุงรักษาเพื่อเพิ่มประสิทธิภาพและความเสถียร</td>
            </tr>
          </tbody>
        </table>
      </div>
    </main>


  </div>
</template>

<script>
export default {
  name: "ProjectTable",
};
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

.sub-title {
  font-size: 1.2rem;
  color: #ffec61;
  margin-top: 10px;
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;

  width: 90%;
  max-width: 1000px;
  padding: 20px 0;
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

table {
  width: 100%;
  border-collapse: collapse;
  color: white;
  text-align: left;
}

th,
td {
  border: 1px solid #00ff80;
  padding: 8px;
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
