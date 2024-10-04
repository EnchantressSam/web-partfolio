<template>
  <section id="projects" class="projects-section">
    <h2>Projects</h2>

    <div class="projects-list">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :image="project.image"
        :video="project.video"
        :modalImage="project.modalImage"
      />
    </div>
  </section>
</template>

<script>
import ProjectCard from './ProjectCard.vue'

export default {
  name: 'ProjectsSection',
  components: {
    ProjectCard
  },
  data () {
    return {
      projects: [
        {
          id: 1,
          title: 'Graphic Design Projects',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, temporibus.',
          image: require('@/assets/keyboard.jpg'), // Статичное изображение
          video: require('@/assets/proj-video1.mp4'), // Видео для запуска по наведению
          modalImage: require('@/assets/code1.png') // Изображение для модального окна
        },
        {
          id: 2,
          title: 'Graphic Design Projects',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, temporibus.',
          image: require('@/assets/keyboard.jpg'),
          video: require('@/assets/proj-video1.mp4'),
          modalImage: require('@/assets/code1.png')
        },
        {
          id: 3,
          title: 'Graphic Design Projects',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, temporibus.',
          image: require('@/assets/keyboard.jpg'),
          video: require('@/assets/proj-video1.mp4'),
          modalImage: require('@/assets/code1.png')
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects-section {
  padding: 50px 0;
  background-color: #f9f9f9;
  text-align: center;
}

.projects-container {
  display: flex;
  justify-content: space-around;
}

.projects-list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

</style>
