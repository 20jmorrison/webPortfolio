<template>

  <div class="parallax">
    <header>
      <img src="@/assets/backback.png" class="parallax-l1">
      <div class="parallax-l2">Jared Morrison's Portfolio</div>
    </header>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@600&family=Secular+One&display=swap" rel="stylesheet">
  </div>

</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>

body {
  margin: 0;
}

.parallax {
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
  perspective: 10px;
}

header {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  transform-style: preserve-3d;
  z-index: -1;
}

.parallax-l1 {
  transform: translateZ(-10px) scale(2);
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
  filter: blur(5px);
}


.parallax-l2 {
  font-size: 7rem;
  color: black;
  font-family: 'Secular One', sans-serif;
}

</style>
