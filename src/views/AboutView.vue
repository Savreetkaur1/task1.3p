<template>
  <div class="about">
    <h1 class="header">ALL ABOUT ME!</h1>
    <h2>{{ message }}</h2>

    <section class="details">
      <div class="background-box">
        <div class="section-wrapper">
      <h3 class="section-title">MY LIFE BACKGORUND</h3>
      <div class="decorative-line"></div>
      <p>I was born in Punjab, a state in India on October 8th, 2004. I moved to Australia for my studies when I was 18 years old. I always had a curiosity and passion to learn more about computers. While studying Information Technology, I started developing an interest in web designing. Hence, I opted for this field as my career.</p>
      </div>
      </div>

      <div class="background-box">
        <div class="section-wrapper">
      <h3 class="section-title">EDUCATIONAL BACKGROUND</h3>
      <div class="decorative-line"></div>
      <p>I studied C and C++ computer languages when I was 17 years old. I came to Australia to pursue my Bachelor's in Information Technology from Deakin University, Melbourne. Over the years, I have developed a strong passion for web development. Not only passion, but my skills have also made great progress. I have gained experience in frontend and backend development. I enjoy taking challenges and experimenting.</p>
      </div>
      </div>

      <div class="background-box">
        <div class="section-wrapper">
      <h3 class="section-title">TECHNICAL SKILLS</h3>
      <div class="decorative-line"></div>
      <p>I have developed a strong passion for web development. Not only passion, but my skills have also made great progress. I have gained experience in frontend and backend development. I enjoy taking challenges and experimenting.</p>
      </div>
      </div>

      <div class="background-box">
        <div class="section-wrapper">
      <h4 class="section-title">MY SKILLS</h4>
      <div class="decorative-line"></div>
      <ul>
        <li>Frontend Development (HTML, CSS, JavaScript)</li>
        <li>Database Management (SQL)</li>
        <li>Backend Development (Node.js)</li>
        <li>Responsive Web Design</li>
        <li>Cybersecurity (Linux)</li>
      </ul>
      </div>
      </div>

      <div class="background-box">
        <div class="section-wrapper">
      <h5 class="section-title">MY PROJECTS</h5>
      <div class="decorative-line"></div>
      <p>I have worked on several projects during my university studies and after my graduation, gaining valuable experience.</p>
      <ul class="projects">
        <li>&#8226;
          <strong>E-commerce website</strong> - Check out
          <a href="https://video.deakin.edu.au/media/t/1_2ye2b7o9">a recording here</a>
        </li>
        <li>&#8226;
          <strong>Javascript</strong> - Check out
          <a href="https://video.deakin.edu.au/media/t/1_9v6q8rj2">a recording here</a>
        </li>
        <li>&#8226;
          <strong>A portfolio website</strong> - Check out
          <a href="https://video.deakin.edu.au/media/t/1_">a recording here</a>
        </li>
      </ul>
      </div>
      </div>
    </section>
    </div>
  
  
</template>

<script setup>
import { ref } from 'vue';
const message = ref('A PASSIONATE WEB DEVELOPER');
</script>

<style scoped>
@media (min-width: 1000px) {
  .about {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content:center;
    min-height: calc(100vh - 6rem); 
    margin-top: 6rem
  }
  .header{
    margin:0;
    padding: 0;
    font-weight: bold;
    color: green;
    transition: color 0.3s;
  }

  .header:hover {
    color: violet;
  }

  .section-wrapper{
    margin-bottom: 20px;
  }

  .section-title{
    font-weight: bold;
    font-size: 1.2rem;
    color: rgb(4, 4, 163)
  }


  .details {
    margin-left: 20px;
  }

  .background-box{
    border:2px solid green;
    padding: 20px;
    background-color: rgb(70, 70, 70);
  }

  .decorative-line{
    width: 100%;
    height: 2px;
    background-color: green;
  }
  
  .projects {
    list-style-type: none;
    padding-left: 20px;
  }

  .projects li {
    margin-bottom: 10px;
  }

  .projects a {
    text-decoration: underline;
    color: yellow;
  }

  .projects a:hover {
    text-decoration: underline;
  }
}
</style>
