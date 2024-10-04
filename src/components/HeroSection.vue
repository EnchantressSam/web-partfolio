<template>
  <section id="hero" class="hero-section">
    <div class="text-container">
      <h1>We are Juniors</h1>
      <p>Driven by curiosity, interns and juniors are coding the future, one line at a time.</p>
      <button>Discover More</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero-section {
  background-image: url('../assets/bg-2.jpg');
  background-size: cover;
  height: 520px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}

.text-container {
  background-color: rgba(0, 0, 0, 0);
  color: white;
  padding: 20px;
  text-align: center;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #ccc;
}
</style>
