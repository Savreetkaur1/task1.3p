<template>
    <div class="contact-form">
      <h2 class="contact-heading">CONTACT ME</h2>
      <form @submit.prevent="submitForm">
    
        <div class="form-section">
          <div class="section-label"> Title: </div>>
          <div class="section-content">
            <input type="radio" id="mr" value="Mr." v-model="formData.title" />
            <label for="mr">Mr.</label>
            <input type="radio" id="mrs" value="Mrs." v-model="formData.title" />
            <label for="mrs">Mrs.</label>
            <input type="radio" id="ms" value="Ms." v-model="formData.title" />
            <label for="ms">Ms.</label>
            <input type="radio" id="none" value="None" v-model="formData.title" />
            <label for="none">None</label>
          </div>
        </div>
  
       
        <div class="form-section">
          <label for="firstName">First Name:</label>
          <input type="text" id="firstName" v-model="formData.firstName" required />
       
          <label for="lastName">Last Name:</label>
          <input type="text" id="lastName" v-model="formData.lastName" required />
      
          <label for="companyName">Company Name:</label>
          <input type="text" id="companyName" v-model="formData.companyName" />
       
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
  
       
        <div class="form-section">
          <label for="subject">Subject:</label>
          <select id="subject" v-model="formData.subject">
            <option value="General Enquiry">General enquiry</option>
            <option value="Feedback">Feedback</option>
            <option value="Support">Support</option>
            <option value="Other">Other</option>
          </select>
        </div>
  
    
        <div class="form-section">
          <label for="message">Write Your Message:</label>
          <textarea id="message" v-model="formData.message" rows="5" required></textarea>
        </div>
  
      
        <div class="form-section">
          <label for="state">Select Your State:</label>
          <select id="state" v-model="formData.state">
            <option value="VIC">Victoria</option>
            <option value="QLD">Queensland</option>
            <option value="NSW">New South Wales</option>
            <option value="SA">South Australia</option>
            <option value="WA">Western Australia</option>
           <option value="NT">Northern Territory</option>
            <option value="ACT">Australian Capital Territory</option>
            <option value="TAS">Tasmania</option>
          </select>
        </div>
  
      
        <div class="form-section">
          <label for="city">City:</label>
          <input type="text" id="city" v-model="formData.city" required />
        </div>
  
       
        <button type="submit" :disabled="submitted">Submit</button>
        <span v-if="submitted">Submitted</span>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const formData = ref({
    title: '',
    firstName: '',
    lastName: '',
    companyName: '',
    email: '',
    subject: 'General Enquiry',
    message: '', 
    state: 'VIC',
    city: '',
  });
  
  const submitted = ref(false);
  
  const submitForm = () => {
   
    console.log('Form submitted with data:', formData.value);
    submitted.value = true;
  };
  </script>
  
  <style scoped>
  .contact-heading {
    font-weight: bold;
    color: green;
    transition: color 0.3s;
  }
     :hover {
    color: yellow;
 }

 :disabled{
    background-color: grey;
    cursor: not-allowed;
 }

 .form-section{
    border: 2px solid green;
    padding: 10px;
    background-color: rgb(58, 57, 57);
    margin-bottom: 10px;
 }

 .form-section input[type="radio"]{
    margin-right: 5px;
 }
 .submit-button{
    background-color: grey;
    color:Green;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    transition: background 0.3s;
 }

  </style>
  