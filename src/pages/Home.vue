<template>
  <section class="section-card">
    <p class="badge">Welcome</p>
    <h1 class="section-title">欢迎来到我的个人网站</h1>
    <p class="muted">
      我是 Pectics，合肥工业大学软件学院的一名软件工程专业学生。这是我的个人展示站点，汇集了我的简介、技术兴趣以及一些感兴趣的项目实践和作品展示。
    </p>
    <p class="muted">
      本页面使用 Vue 3 和 Vite 构建，旨在提供简洁清晰的浏览体验。
    </p>
    <div class="keywords">
      <span v-for="tag in tags" :key="tag" class="keyword">{{ tag }}</span>
    </div>
    <RouterLink to="/about" class="button">了解我的更多信息 →</RouterLink>
  </section>
</template>

<script setup>
const tags = ['Java', 'Kotlin', 'Spring Boot', 'C++', 'Vue3', 'ASM']
</script>

<style scoped>
.keywords {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 0.8rem;
}

.keyword {
  padding: 0.35rem 0.7rem;
  border-radius: 999px;
  background: #f0f4ff;
  color: #3f51b5;
  font-weight: 700;
  font-size: 0.95rem;
}
</style>
