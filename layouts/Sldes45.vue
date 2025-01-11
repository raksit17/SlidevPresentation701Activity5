<template>
  <div class="green-layout">
    <header class="layout-header">
      <h1 class="main-title">การจัดกลุ่มบทความตามเกณฑ์</h1>
    </header>
    <main class="layout-content">
      <div class="section-container">
        <!-- การพัฒนาเครื่องมือผู้ช่วยเสมือนอัจฉริยะด้วย LLM -->
        <div class="content-section">
          <h2 class="section-title">กลุ่มผู้ช่วยเสมือนอัจฉริยะ</h2>
          <ul>
            <li v-for="article in groupedArticles['การพัฒนาเครื่องมือผู้ช่วยเสมือนอัจฉริยะด้วย LLM']" :key="article.title">
              <strong>บทความ:</strong> {{ article.title }}<br />
              <strong>เนื้อหา:</strong> {{ article.content }}
            </li>
          </ul>
        </div>

        <!-- การจัดการงานและการบริหารเวลา -->
        <div class="content-section">
          <h2 class="section-title">กลุ่มการจัดการเวลา</h2>
          <ul>
            <li v-for="article in groupedArticles['การจัดการงานและการบริหารเวลา']" :key="article.title">
              <strong>บทความ:</strong> {{ article.title }}<br />
              <strong>เนื้อหา:</strong> {{ article.content }}
            </li>
          </ul>
        </div>

        <!-- การประยุกต์ใช้ AI ในการจัดการส่วนตัว -->
        <div class="content-section">
          <h2 class="section-title">กลุ่มผู้ช่วยส่วนตัว</h2>
          <ul>
            <li v-for="article in groupedArticles['การประยุกต์ใช้ AI ในการจัดการส่วนตัว']" :key="article.title">
              <strong>บทความ:</strong> {{ article.title }}<br />
              <strong>เนื้อหา:</strong> {{ article.content }}
            </li>
          </ul>
        </div>
      </div>
    </main>

  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          title: "Intelligent Virtual Assistants with LLM-based Process Automation",
          content: "การใช้โมเดลภาษาใหญ่ (LLM) เพื่อพัฒนาผู้ช่วยเสมือนที่สามารถดำเนินงานที่ซับซ้อนได้ เช่น การใช้งานแอปพลิเคชันมือถือ การจัดการ UI และการดำเนินการตามคำสั่งผู้ใช้.",
          category: "การพัฒนาเครื่องมือผู้ช่วยเสมือนอัจฉริยะด้วย LLM",
        },
        {
          title: "AutoDroid: LLM-powered Task Automation in Android",
          content: "การใช้โมเดลภาษาใหญ่ (LLM) เพื่อพัฒนาผู้ช่วยเสมือนที่สามารถดำเนินงานที่ซับซ้อนได้ เช่น การใช้งานแอปพลิเคชันมือถือ การจัดการ UI และการดำเนินการตามคำสั่งผู้ใช้.",
          category: "การพัฒนาเครื่องมือผู้ช่วยเสมือนอัจฉริยะด้วย LLM",
        },
        {
          title: "TIME LINE SCHEDULER USING AI",
          content: "การพัฒนาระบบจัดการงานและตารางเวลาโดยใช้ AI และการเพิ่มประสิทธิภาพ.",
          category: "การจัดการงานและการบริหารเวลา",
        },
    
      ],
    };
  },
  computed: {
    groupedArticles() {
      return this.articles.reduce((groups, article) => {
        if (!groups[article.category]) {
          groups[article.category] = [];
        }
        groups[article.category].push(article);
        return groups;
      }, {});
    },
  },
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

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 90%;
  max-width: 1000px;
  padding: 20px 0;
}

.section-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 16px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 1.0);
  padding: 6px;
  text-align: left;
  font-size: 0.9rem;
}

.section-title {
  font-size: 1.1rem;
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
