<template>
  <section class="section-card home">
    <p class="badge">欢迎</p>
    <h1 class="section-title">欢迎来到我的个人网站</h1>
    <p class="muted">
      我是 Pectics，来自合肥工业大学软件学院的软件工程专业，热爱 Vue、前端工程化以及 Minecraft 插件。
      这个小站用来收纳我的简介与项目作品，也记录我一路的成长脚印。
    </p>
    <div class="keywords">
      <span v-for="tag in tags" :key="tag" class="keyword">{{ tag }}</span>
    </div>
    <RouterLink to="/about" class="button">了解我的更多信息 →</RouterLink>
  </section>
</template>

<script setup>
const tags = ['Vue3', '前端工程化', '校园开发', '创意玩法设计']
</script>

<style scoped>
.home {
  display: grid;
  gap: 1.25rem;
}

.keywords {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
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
