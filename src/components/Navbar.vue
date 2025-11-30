<template>
  <header class="navbar">
    <div class="nav-inner">
      <RouterLink to="/" class="brand">
        <span class="badge">Pectics</span>
        <span class="brand-name">个人网站</span>
      </RouterLink>
      <nav class="nav-links">
        <RouterLink v-for="item in navItems" :key="item.to" :to="item.to" class="nav-link">
          {{ item.label }}
        </RouterLink>
      </nav>
    </div>
  </header>
</template>

<script setup>
const navItems = [
  { label: 'Home', to: '/' },
  { label: 'About', to: '/about' },
  { label: 'Projects', to: '/projects' },
]
</script>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 10;
  background: #f7f9fb;
  border-bottom: 1px solid #e6ebf2;
  backdrop-filter: blur(8px);
}

.nav-inner {
  width: min(1100px, 100%);
  margin: 0 auto;
  padding: 1rem 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 800;
  color: #1f2a3d;
}

.brand-name {
  font-size: 1.05rem;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.nav-link {
  padding: 0.45rem 0.9rem;
  border-radius: 12px;
  color: #1f2a3d;
  font-weight: 600;
  transition: background 0.2s ease, color 0.2s ease;
}

.nav-link:hover {
  background: #eef2ff;
  color: #4f46e5;
}

.nav-link.is-active {
  background: linear-gradient(135deg, #5c7cfa, #6dd5ed);
  color: #ffffff;
  box-shadow: 0 10px 24px rgba(93, 124, 250, 0.3);
}
</style>
