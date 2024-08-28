<!-- ContactUs.vue -->
<template>
  <div class="contact-us-container">
    <h1 class="contact-us-title">Get in Touch</h1>
    <p class="contact-us-description">
      Give us a call or submit your information using the form below.
    </p>

    <!-- Cards for Contact Information -->
    <div class="cards-container">

      <div class="info-card">
        <h2 class="card-title">Our Loacation</h2>
        <p class="card-text">Call us at: (123) 456-7890</p>
      </div>

      <div class="info-card">
        <h2 class="card-title">Phone</h2>
        <p class="card-text">Call us at: (123) 456-7890</p>
      </div>

      <div class="info-card">
        <h2 class="card-title">Service Area</h2>
        <p class="card-text">Serving the Triangle Area and surrounding communities.</p>
      </div>
      <div class="info-card">
        <h2 class="card-title">Payment Accepted</h2>
        <p class="card-text"></p>
      </div>

      <div class="info-card">
        <h2 class="card-title">Hours</h2>
        <p class="card-text">Monday - Friday: 9:00 AM - 5:00 PM</p>
        <p class="card-text">Saturday: 9:00 AM - 1:00 PM</p>
        <p class="card-text">Sunday: Closed</p>
      </div>
    </div>

    <!-- Contact Form -->
    <form class="contact-form" @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" v-model="name" placeholder="Your Name" required />
      </div>

      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="email" placeholder="Your Email" required />
      </div>

      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" v-model="message" rows="4" placeholder="Your Message" required></textarea>
      </div>

      <button type="submit" class="submit-button">Get in Touch</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Define reactive form fields
const name = ref('');
const email = ref('');
const message = ref('');

// Form submission handler
const submitForm = () => {
  console.log('Form submitted:', { name: name.value, email: email.value, message: message.value });
  // You can handle form submission here, such as sending data to a server
};
</script>

<style scoped>
.contact-us-container {

  margin: 0 auto;
  padding: 20px;
  background-color: #fff5e1; /* Light gold background */
  border: 2px solid #d4af37; /* Gold border */
  border-radius: 8px;
  text-align: center;
}

.contact-us-title {
  font-size: 32px;
  color: #333;
  margin-bottom: 15px;
}

.contact-us-description {
  font-size: 18px;
  color: #666;
  margin-bottom: 25px;
}

.cards-container {
  display: flex;
  justify-content: space-around;
  gap: 15px;
  margin-bottom: 30px;
  flex-wrap: wrap;
}

.info-card {
  background-color: #ffffff;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  width: 250px;
  text-align: left;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card-title {
  font-size: 20px;
  color: #b22222; /* Dark red color */
  margin-bottom: 10px;
}

.card-text {
  font-size: 16px;
  color: #333;
}

.contact-form {
  margin-top: 30px;
}

.form-group {
  margin-bottom: 20px;
  text-align: left;
}

label {
  display: block;
  font-size: 14px;
  color: #333;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

.submit-button {
  background-color: #b22222; /* Red color */
  color: white;
  padding: 12px 20px;
  font-size: 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.submit-button:hover {
  background-color: #8b0000; /* Darker red on hover */
}
</style>

  