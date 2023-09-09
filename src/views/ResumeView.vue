<template>
    <div class="resume-page">
      <section>
        <h2>Contact Information</h2>
        <button @click="showContactInfo = !showContactInfo">Show/Hide</button>
        <table v-if="showContactInfo">
          <tr>
            <th>My Name</th>
            <td>{{ contactInfo.name }}</td>
          </tr>
          <tr>
            <th>My Phone</th>
            <td>{{ contactInfo.phone }}</td>
          </tr>
          <tr>
            <th>My Email</th>
            <td>{{ contactInfo.email }}</td>
          </tr>
          <tr>
            <th>My Address</th>
            <td>{{ contactInfo.address }}</td>
          </tr>
          <tr>
            <th>My linkedIn</th>
            <td><a href="https://linkedIn.com" target="_blank">{{ contactInfo.linkedin }}</a></td>
          </tr>
        </table>
      </section>
  
      
      <section>
        <h2>My Skills</h2>
        <button @click="showSkills = !showSkills">Show/Hide</button>
        <table v-if="showSkills">
          <tr v-for="(skill, index) in skills" :key="index">
            <td>{{ skill }}</td>
          </tr>
        </table>
      </section>
  
   
      <section>
        <h2>My Education</h2>
        <button @click="showEducation = !showEducation">Show/Hide</button>
        <table v-if="showEducation">
          <tr v-for="(edu, index) in education" :key="index">
            <th>Degree</th>
            <td>{{ edu.degree }}</td>
            <th>Institution</th>
            <td>{{ edu.institution }}</td>
            <th>Year</th>
            <td>{{ edu.year }}</td>
          </tr>
        </table>
      </section>
  
     
      <section>
        <h2>Work Experience</h2>
        <button @click="showWorkExperience = !showWorkExperience">Show/Hide</button>
        <table v-if="showWorkExperience">
          <tr v-for="(job, index) in workExperience" :key="index">
            <th>Position</th>
            <td>{{ job.position }}</td>
            <th>Year</th>
            <td>{{ job.year }}</td>
            <th>Company</th>
            <td>{{ job.company }}</td>
           
          </tr>
        </table>
      </section>
  
   
      <section>
        <h2>Certifications</h2>
        <button @click="showCertifications = !showCertifications">Show/Hide</button>
        <ul v-if="showCertifications">
          <li v-for="(certification, index) in certifications" :key="index">{{ certification }}</li>
        </ul>
      </section>
  

  
     
      <section>
        <h2>Languages Spoken</h2>
        <button @click="showLanguages = !showLanguages">Show/Hide</button>
        <ul v-if="showLanguages">
          <li v-for="(language, index) in languages" :key="index">{{ language }}</li>
        </ul>
      </section>
  
      <section>
        <h2>Hobbies and Interests</h2>
        <button @click="showHobbies = !showHobbies">Show/Hide</button>
        <ul v-if="showHobbies">
          <li v-for="(interest, index) in hobbies" :key="index">{{ interest }}</li>
        </ul>
      </section>
  
     
      <section>
        <h2>References</h2>
        <button @click="showReferences = !showReferences">Show/Hide</button>
        <p v-if="showReferences">Email to request references</p>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showContactInfo: true,
        showSkills: true,
        showEducation: true,
        showWorkExperience: true,
        showCertifications: true,
        showLanguages: true,
        showHobbies: true,
        showReferences: true,
     
        contactInfo: {
          name: "Savreet Kaur Somal",
          phone: "563-373-xxx",
          email: "savreet***@email.com",
          address: "123 Main St, San Francisco, CA 94107",
          linkedin: "savreet",
        },
        skills: ["HTML", "JavaScript", "CSS", "Vue.js", "Node.js"],
        education: [
          {
            degree: "Bachelor in information technology",
            institution: "Deakin University",
            year: "2023",
          },
          {
            degree: "Master's in information technology",
            institution: "Deakin University",
            year: "2028",
          },
        
        ],
        workExperience: [
          {
            position: "Web Developer",
            company: "youtube",
            year: "2023 - Present",
          },
        
        ],
        certifications: ["Certification 1", "Certification 2"],
        languages: ["English", "Hindi", "Punjabi"],
        hobbies: ["Reading", "travel"],
       
      };
    },
  };
  </script>
  
  <style scoped>
.resume-page{
    margin-top: 6rem;
    font-family: Arial;
    max-width: 800px;
    margin: 1 rem auto;
}

section{
    margin-bottom: 20px;
}

table{
    width:100%;
    border-collapse: collapse;
    border: 1px solid white;
}

th, td{
    padding: 10px;
    text-align: left;
    border: 1px solid white;
}

th{
    background-color: green;
}

button{
    background-color:blue;
    color:white;
    border:none;
    padding: 10px 20px;
    cursor: pointer;
}

button:hover{
    background: pink;
}

a{
    text-decoration: underline;
    color: brown;
}

a:hover{
    text-decoration: underline;
}
  </style>
  