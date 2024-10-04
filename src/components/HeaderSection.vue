<template>
  <header>
        <nav>
      <ul>
        <!-- <li><a @click="scrollTo('hero')">About</a></li> -->
        <li><a href="#about">About</a></li>
        <!-- <li><a @click="scrollTo('projects')">Projects</a></li> -->
        <li><a href="#projects">Projects</a></li>
        <!-- <li><a @click="scrollTo('contacts')">Contact</a></li> -->
        <li><a href="#contacts">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>

export default {
  name: 'HeaderSection'

}
</script>

<style scoped>
header {
  background-color: #2A282B;
  padding: 15px;
  text-align: center;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-size: 18px;
  cursor: pointer;
}

nav ul li a:hover {
  text-decoration: underline;
}
</style>
