<template>
  <div class="green-layout">
    <!-- Header -->
    



  </div>
</template>

<script setup>

</script>

<style scoped>
.green-layout {
  background-image: url('/assets/images/flow1.png');
  background-size: 100% 550px;
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





.layout-content {
  background-image: url('/assets/images/flow.png');
  background-size: contain; /* ปรับภาพให้พอดีกับพื้นที่ */
  background-position: center;
  background-color: rgba(0, 0, 0, 0.7);

  display: flex;
  flex-direction: column;
height: 100%;
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
