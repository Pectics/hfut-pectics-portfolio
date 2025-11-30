<template>
  <section class="section-card">
    <p class="badge">About</p>
    <h1 class="section-title">关于我的</h1>
    <div class="grid grid-2">
      <div>
        <p class="muted">基本信息</p>
        <ul class="info-list">
          <li><strong>姓名：</strong> {{ name }}</li>
          <li><strong>学校：</strong> 合肥工业大学 软件学院</li>
          <li><strong>专业：</strong> 软件工程</li>
          <li><strong>学号：</strong> {{ id }}</li>
        </ul>
      </div>
      <div>
        <p class="muted">技术兴趣</p>
        <ul class="info-list">
          <li>Java/Kotlin 及其生态</li>
          <li>Node.js 脚本与前端工程化</li>
          <li>Minecraft 插件开发设计</li>
          <li>校园生活实用工具</li>
        </ul>
      </div>
    </div>
    <p class="muted">
      我相信清晰、简洁的产品体验能帮助更多人专注在真正重要的事情上。<br>希望通过不断实践，把创意落地成看得见、用得上的作品。
    </p>
  </section>
</template>

<script setup>
const name = import.meta.env.VITE_NAME;
const id = import.meta.env.VITE_ID;
</script>

<style scoped>
.info-list {
  padding-left: 1rem;
  margin: 0.4rem 0 0;
  display: grid;
  gap: 0.45rem;
  color: #1f2a3d;
}
</style>
