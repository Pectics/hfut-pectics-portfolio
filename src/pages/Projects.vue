<template>
  <section class="section-card">
    <p class="badge">Projects</p>
    <h1 class="section-title">个人作品</h1>
    <p class="muted">以下项目通过简单的数组数据驱动渲染，展示了我在兴趣方向的实践。</p>
    <div class="grid" style="margin-top: 1rem;">
      <article v-for="project in projects" :key="project.name" class="project">
        <div class="project-header">
          <h3>{{ project.name }}</h3>
          <a v-if="project.link" class="project-link" :href="project.link" target="_blank" rel="noreferrer">
            查看详情 →
          </a>
        </div>
        <p class="muted">{{ project.desc }}</p>
      </article>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    name: 'hfut-info：工大公开信息查询接口',
    desc: '对工大的公开数据进行查询、整合、格式化，并提供一套便捷的接口服务。',
    link: 'https://github.com/Pectics/hfut-info',
  },
  {
    name: 'hfutnet：工大的校园网自动登录连接工具',
    desc: '使用C++编写的校园网登录工具，避免了手动在浏览器登录的繁琐操作。',
    link: 'https://github.com/Pectics/hfutnet',
  },
  {
    name: 'PermPacks：基于权限节点的 Minecraft 资源包栈管理插件',
    desc: '使用 Kotlin 编写的用于管理 Minecraft 服务器中玩家资源包栈的插件，支持对象存储服务的自动对接。',
    link: 'https://github.com/Pectics/PermPacks',
  },
]
</script>

<style scoped>
.project {
  padding: 1rem;
  border: 1px solid #e6ebf2;
  border-radius: 12px;
  background: linear-gradient(180deg, #ffffff 0%, #f9fbff 100%);
}

.project-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  margin-bottom: 0.35rem;
}

.project-header h3 {
  margin: 0;
  font-size: 1.1rem;
}

.project-link {
  color: #4f46e5;
  font-weight: 700;
}
</style>
