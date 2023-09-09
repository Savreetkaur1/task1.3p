<script setup>
import TheWelcome from '../components/TheWelcome.vue'
</script>

<template>
  <main>
    <img src="homepage.png" alt="Rectangle Image" class="rectangle-image"/>
    <section class="basic-details">
      <h2 class="welcome-text"><u><strong style="color: red;">WELCOME TO MY PORTFOLIO WEBPAGE</strong></u></h2>
    </section>

    <div class="description-box">
      <p><strong style="color:green;">ALLOW ME TO GIVE A BRIEF DESCRIPTION ABOUT MYSELF</strong></p>
      <p>
        I am obsessed with making things and even more obsessed with making things better. I have always been creative. I decided that I wanted be a web developer when I was 12. After graduating from Deakin University, Waurn Ponds, Melbourne, I've been actively involved in the web design community for the lst 7 years. My speciality is front-end web desgin and development, making pixel magic in photoshop and turning it into beautiful, unique HTML & CSS. 

      </p>
      <p>When I am not designing, I would be reading, watching web series, playing badminton.</p>

      <p>Talking about my learning resources, some of the major learning resouces were
        <a href="https://www.youtube.com/" target="_blank" style="color: blue; text decoration: underline;">Youtube</a> for all the youtube tutorials, and
        <a href="https://w3schools.com/" target="_blank" style="color: blue; text decoration: underline;">W3 Schools</a> for all the w3 schools tutorials.
      </p>
    </div>
    
    <img src="web.jpeg" alt="right image" class="right-image"/>

    <TheWelcome />
  </main>
</template>

<style scoped>
.welcome-text {
  animation: moveWelcome 5s linear infinite;
}
@keyframes moveWelcome {
  0% {
    transform: translateX(-100%);
  }
  100%{
    transform: translateX(100%);
  }
}
.rectangle-image{
  width: 100%;
  max-width: 100%;
  height: auto;
  display: block;
  margin-top: 1rem;
}

.right-image{
  /*float: right; */
  width:200px;
  margin-left:1rem;
  margin-top:1rem;
}

.description-box {
  background-color:rgb(77, 76, 76);
  padding: 1rem;
  border: 1px solid;
  border-radius: 5px;
  margin-top: 1rem;
}

.description.box p{
  margin:0;
}
</style>