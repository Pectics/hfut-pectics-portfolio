<template>
  <footer class="footer">
    <div class="footer-inner">
      <p class="muted">© 2024 Pectics · 合肥工业大学软件学院</p>
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
  padding: 1.25rem 1rem 2rem;
}

.footer-inner {
  width: min(1100px, 100%);
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  font-size: 0.95rem;
}
</style>
