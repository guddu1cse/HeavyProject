<script>
export default {
  data() {
    return {
      name: 'Bada Wala Project In Vue.js',
      title: 'Heavy Project',
      description:
        'HeavyProject is a learning-focused project built to practice and strengthen core development skills. It is used to explore concepts step by step, experiment with features, and gain hands-on experience by building and improving real functionality during the learning process.',
      langauge: ['Spring Boot', 'Node.js', 'Data Structure & Algorithm', 'Vue.js', 'React.js', 'Angular', 'MongoDB', 'MySQL'],
      btn_name: 'Tip',
      portfolio_link: 'https://guddu1cse.github.io/myportfolio',
      resume_link: 'https://hackerrank-resume.s3.us-east-1.amazonaws.com/uploads/9758288/OTc1ODI4OA==.pdf',
      count: 0
    }
  },

  methods: {
    btnTip() {
      if(this.count >=4){
        this.btn_name = "Ruk ja abb!";
      } else if(this.btn_name === 'Tip'){
        this.btn_name = 'Tap';
      } else {
         this.btn_name = 'Tip';
      }
      this.count++;
    },

    reset() {
      this.count = 0;
      this.btn_name = 'Tip';
    }
  }
}
</script>

<template>
  <div class="container">
    <h1 class="title">{{ name }}</h1>
    <h3 class="title">{{ title }}</h3>
    <p class="desc">{{ description }}</p>
     <ul class="tech-list">
      <li v-for="(value, index) in langauge" :key="index">
        {{ value }}
      </li>
    </ul>

    <button class="btn" v-on:click="btnTip">
      {{ btn_name }}
    </button>
    <button v-if="count >= 4" class="btn" v-on:click="reset">Clear Kar Do!</button>
    <div class="links">
      <a :href="portfolio_link" target="_blank">Portfolio</a>
      <a :href="resume_link" target="_blank">Resume</a>
    </div>
  </div>
</template>

<style scoped>
/* main dabba */
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  padding: clamp(16px, 5vw, 40px);
  text-align: center;

  background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
}

.title {
  /* thoda style wala font */
  font-size: clamp(1.8rem, 4vw, 3rem);
  font-weight: 800;
  letter-spacing: 1px;
  margin-bottom: 20px;

  /* chamkauaaa color */
  background: linear-gradient(90deg, #a855f7, #ec4899);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.desc {
  width: 100%;
  max-width: 900px;
  font-size: clamp(0.95rem, 2.5vw, 1.2rem);
  line-height: 1.8;
  color: #e5e7eb;
  background: rgba(255, 255, 255, 0.08);
  padding: clamp(16px, 4vw, 32px);
  border-radius: 16px;
  backdrop-filter: blur(10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.35);
}

/* chotka scree ke lia */
@media (max-width: 480px) {
  .title {
    letter-spacing: 0.5px;
  }

  .desc {
    line-height: 1.6;
  }
}

/* badka screen ke lia */
@media (min-width: 1200px) {
  .container {
    padding-top: 80px;
    padding-bottom: 80px;
  }
}

.subtitle {
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 20px;
  color: #e0e7ff;
}

.tech-list {
  margin-top: 24px;
  padding-left: 20px;
  text-align: left;
  max-width: 900px;
  width: 100%;
}

.tech-list li {
  font-size: 1rem;
  line-height: 1.8;
  color: #f1f5f9;
  margin-bottom: 8px;
}

/* badka screen ke lia */
@media (max-width: 480px) {
  .tech-list {
    padding-left: 16px;
  }

  .tech-list li {
    font-size: 0.95rem;
  }

  .btn {
    width: 100%;
  }
}

.btn {
  margin-top: 24px;
  padding: 10px 20px;

  font-size: 1rem;
  font-weight: 600;

  color: #ffffff;
  background-color: #4f46e5;

  border: none;
  border-radius: 6px;
  cursor: pointer;

  transition: background-color 0.25s ease, transform 0.15s ease;
}


.links {
  margin-top: 20px;
}

.links a {
  margin-right: 16px;
  color: #2563eb;          /* normal blue */
  text-decoration: underline;
  font-size: 1rem;
}

.links a:hover {
  color: #1d4ed8;
}


</style>