<template>
    <section id="about" class="about-section">
      <div class="about-content">
        <h2>About</h2>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptatem molestiae consequatur pariatur modi aliquam inventore quae repellendus asperiores quos sequi nam cumque similique necessitatibus magnam tenetur, laborum laboriosam nisi? Ut ipsam quidem, necessitatibus eum nemo voluptatibus ipsa sequi quaerat rerum repellat ex, hic quibusdam illum. Voluptatibus, veritatis soluta.
        </p>
      </div>
    </section>
  </template>

<script>
export default {
  name: 'AboutSection'
}
</script>

  <style scoped>
  .about-section {
    background-color: #7ec3ff; /* Голубой фон */
    padding: 90px 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .about-content {
    width: 80%; /* Ширина секции AboutSection будет такой же, как у ProjectsSection */
    max-width: 1200px; /* Максимальная ширина для больших экранов */
    text-align: center;
    color: #333; /* Цвет текста */
  }

  h2 {
    font-size: 2.5em;
    margin-bottom: 20px;
  }

  p {
    font-size: 1.2em;
    line-height: 1.6;
    max-width: 800px;
    margin: 0 auto;
  }
  </style>
