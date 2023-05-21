<template>
  <div class="wrapper">
    <div class="stickyHeader">
      <div class="quickLinks">
        <button class="goTohome" @click="scrollTohome()">Home</button>
        <button class="goTowhoami" @click="scrollTowhoami()">About Me</button>
        <button class="goToprojects" @click="scrollToprojects()">Projects</button>
        <button class="downloadResume" @click="downloadResumePDF()">Download Resume PDF</button>
      </div>
    </div>
    <header class="home">
      <img src="@/assets/backback.png" class="parallax-l1" />
      <div class="parallax-l2">
        <p class="title">Jared Morrison's Portfolio</p>
        <div class="scrollDownPrompt">
          <iframe src="https://giphy.com/embed/mjRKIiDIzryBxbimeq" frameBorder="0" class="giphy-embed"
            allowFullScreen></iframe>
          <div>Scroll Down</div>
        </div>
      </div>
    </header>

    <section class="whoami">
      <p>whoami?</p>
      <p class="whoBody">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec aliquam sollicitudin nibh vitae
        feugiat. Donec auctor lacinia lacus at suscipit. Suspendisse eget sollicitudin lectus. Cras vitae massa orci.
        Integer faucibus mollis mattis. Curabitur maximus nisl eget viverra elementum. Vestibulum iaculis ante risus, sed
        commodo nisi tempus eget. Proin nisi nisl, dignissim nec condimentum eu, lacinia quis libero. Proin egestas
        facilisis eros, eu molestie enim lacinia ac. Morbi pharetra eros lobortis, ornare eros a, luctus felis. Nulla eu
        elit vitae mi vehicula rutrum sed ac quam. Maecenas eu elit eu lectus pulvinar fringilla ut a enim. Ut blandit sem
        massa, ut vehicula leo commodo in.</p>

    </section>

    <section class="projects">
      <img src="@/assets/gradi.jpg" class="parallax-l1 grad" />
      <div class="parallax-l2 proj">
        <p class="title">Projects</p>
      </div>
    </section>

    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@600&family=Secular+One&display=swap"
      rel="stylesheet" />
  </div>
</template>

<script>
import resumePDF from "@/assets/Jared_Morrison_Resume.pdf";
export default {
  name: "App",
  components: {},
  methods: {
    scrollTohome() {
      const element = document.getElementsByClassName('home')[0];
      element.scrollIntoView({ behavior: 'smooth' });
    },
    scrollTowhoami() {
      const element = document.getElementsByClassName('whoami')[0];
      element.scrollIntoView({ behavior: 'smooth' });
    },
    scrollToprojects() {
      const element = document.getElementsByClassName('projects')[0];
      element.scrollIntoView({ behavior: 'smooth' });
    },
    downloadResumePDF() {
      const link = document.createElement("a");
      link.href = resumePDF; // Set the href attribute to the file path
      link.download = "resume.pdf"; // Set the download attribute to the desired file name

      // Append the <a> element to the document body
      document.body.appendChild(link);

      // Trigger the click event on the <a> element to start the download
      link.click();

      // Clean up by removing the temporary <a> element
      document.body.removeChild(link);
    }
  }
};
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
  transform: translateZ(-5px) scale(1.5);
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
  filter: blur(10px);
}

.parallax-l2 {
  margin-top: -10vh;
  color: black;
  font-family: "Secular One", sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title {
  margin: 0;
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

.whoami {
  font-family: "Secular One", sans-serif;
  font-size: 3vw;
  line-height: 7vh;
  padding: 2rem;
  background-color: #333;
  color: white;
  height: 85vh;
  padding: 10vh;
}

.whoBody {
  font-size: 2vw;
}

.projects {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  margin-top: 50vh;
  transform-style: preserve-3d;
  z-index: -1;
}

.grad {
  width: 110vw;
  height: 200vh;
}

.proj {

  position: sticky;
  margin-top: -150vh;
  position: -webkit-sticky;
  top: 0;
  padding: 40px;
}

.stickyHeader {
  position: sticky;
  position: -webkit-sticky;
  padding: 10px;
  top: 0;
  display: flex;
  flex-direction: column;
}

.quickLinks {
  align-self: flex-end;
}

.goTohome,
.goTowhoami,
.goToprojects,
.downloadResume {
  font-family: "Secular One", sans-serif;
  align-self: flex-end;
  background: transparent;
  border: none;
  text-decoration: underline;
  cursor: pointer;
}
</style>
