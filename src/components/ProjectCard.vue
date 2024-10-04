<template>
    <div class="project-card">
      <!-- Контейнер для изображения и видео -->
      <div
        class="project-media"
        @mouseenter="hovering = true"
        @mouseleave="hovering = false"
        @click="showModal = true"
      >
        <!-- Показываем изображение, если мышь не наведена -->
        <img
          v-if="!hovering"
          :src="image"
          alt="Project image"
          class="project-image"
        />
        <!-- Показываем видео, если мышь наведена -->
        <video
          v-if="hovering"
          :src="video"
          autoplay
          muted
          loop
          class="project-video"
        />
      </div>

      <h3 class="project-title">{{ title }}</h3>
      <p class="project-description">{{ description }}</p>

      <!-- Модальное окно -->
      <div v-if="showModal" class="modal-overlay" @click="showModal = false">
        <div class="modal-content" @click.stop>
          <span class="close-button" @click="showModal = false">&times;</span>
          <!-- Прокручиваемый контент внутри модального окна -->
          <div class="scrollable-content">
            <img :src="modalImage" alt="Code example" class="modal-image"/>
          </div>
        </div>
      </div>
    </div>
  </template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    video: {
      type: String,
      required: true
    },
    modalImage: {
      type: String,
      required: true
    }
  },
  data () {
    return {
      hovering: false, // Для отслеживания наведения мыши
      showModal: false // Для отображения модального окна
    }
  }
}
</script>

  <style scoped>
  .project-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 16px;
    text-align: center;
    background-color: #fff;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
    position: relative;
  }

  .project-card:hover {
    transform: scale(1.05);
  }

  .project-image, .project-video {
    width: 100%;
    height: auto;
    border-radius: 4px;
    margin-bottom: 16px;
  }

  .project-title {
    font-size: 22px;
    margin: 0;
    color: #333;
  }

  .project-description {
    font-size: 16px;
    color: #666;
  }

  /* Модальное окно */
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }

  .modal-content {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    width: 80%;
    max-height: 80%;
    position: relative;
  }

  .scrollable-content {
    max-height: 60vh;
    overflow-y: auto;
  }

  .modal-image {
    width: 100%;
  }

  .close-button {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 24px;
    cursor: pointer;
    color: #333;
  }
  </style>
