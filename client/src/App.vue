<template>

  <div class="wrapper">

    <header>
      <img src="@/assets/backback.png" class="parallax-l1">
      <div class="parallax-l2">
        <p class="title">Jared Morrison's Portfolio</p>
        <div class="scrollDownPrompt">
          <iframe src="https://giphy.com/embed/mjRKIiDIzryBxbimeq" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
          <div>Scroll Down</div>
        </div>
      </div>
      
    </header>
    <section>
        whoami? 
    </section>

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

.wrapper {
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
  perspective: 10px;
}

header {
  position: relative;
  display: flex;
  flex-direction: column;
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
  filter: blur(10px);
}


.parallax-l2 {
  color: black;
  font-family: 'Secular One', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title {
  margin: 0px;
  font-size: 3.8vw;

}

.scrollDownPrompt {
  position: relative;
  font-size: 0.7vw;
  width: 100vw;
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.giphy-embed {
  width: 2vw;
  height: 2vw;
}

section {
  font-size: 2rem;
  padding: 2rem;
  background-color: #333;
  color: white;
  height: 200vh;
}

</style>
