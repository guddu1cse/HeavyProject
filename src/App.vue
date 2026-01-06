<script>
export default {
  data() {
    return {
      name: 'Bada Wala Project In Vue.js',
      description: 'HeavyProject is a learning-focused project built to practice and strengthen core development skills. It is used to explore concepts step by step, experiment with features, and gain hands-on experience by building and improving real functionality during the learning process.'
    }
  }
}
</script>

<template>
  <div class="container">
    <h1 class="title">{{ name }}</h1>
    <p class="desc">{{ description }}</p>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.container {
  /* display: flex; */
  justify-content: center;
  align-items: center;
  gap: 16px;
}

.title {
  color: #6a0dad;
}

.desc {
  color: #2e8b57;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
