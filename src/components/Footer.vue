<template>
  <footer class="footer">
    <div class="footer-inner">
      <p class="muted">© {{ new Date().getFullYear() }} Pectics · 合肥工业大学软件学院</p>
      <p class="muted">用 Vue 3 + Vite 构建的个人展示站点</p>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  border-top: 1px solid #e6ebf2;
  background: #f7f9fb;
  padding: 2rem 2rem 1.6rem;
}

.footer-inner {
  width: min(1000px, 100%);
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  font-size: 0.8rem;
}
</style>
