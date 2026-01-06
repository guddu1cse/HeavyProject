<script>
export default {
  data() {
    return {
      name: 'Bada Wala Project In Vue.js',
      title: 'HeavyProject',
      description:
        'HeavyProject is a learning-focused project built to practice and strengthen core development skills. It is used to explore concepts step by step, experiment with features, and gain hands-on experience by building and improving real functionality during the learning process.'
    }
  }
}
</script>

<template>
  <div class="container">
    <h1 class="title">{{ name }}</h1>
    <h3 class="title">{{ title }}</h3>
    <p class="desc">{{ description }}</p>
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
</style>
