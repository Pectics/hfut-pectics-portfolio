<template>
  <section class="section-card projects">
    <p class="badge">Projects</p>
    <h1 class="section-title">个人作品</h1>
    <p class="muted">以下项目通过简单的数组数据驱动渲染，展示了我在校园及兴趣方向的实践。</p>
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
    name: '校园日程提醒小程序',
    desc: '用 Vue 组件封装课表与 ToDo 模块，方便同学快速查看当天安排。',
    link: 'https://example.com/schedule',
  },
  {
    name: 'Minecraft 服务器小游戏插件',
    desc: '设计玩法逻辑并实现排行榜、奖励等功能，提升玩家互动乐趣。',
  },
  {
    name: '个人作品集网站',
    desc: '基于 Vue 3 + Vite 构建的展示型网站，聚合了我的简介与项目亮点。',
    link: 'https://example.com/portfolio',
  },
]
</script>

<style scoped>
.projects {
  display: grid;
  gap: 1rem;
}

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
