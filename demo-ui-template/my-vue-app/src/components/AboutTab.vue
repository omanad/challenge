<!-- AboutUs.vue -->
<template>
  <div class="about-us-container">
    <h1 class="about-us-title">About Us</h1>
    <p class="about-us-description">
      At Dent Busters, we specialize in paintless dent removal with over 25 years of expertise. Our team of professionals is dedicated to restoring the value and appearance of your car using advanced techniques that preserve your car's original finish.
    </p>
    <div class="button-container">
      <button class="action-button call-us">Call Us</button>
      <button class="action-button contact-us">Contact Us</button>
      <button class="action-button schedule-service">Schedule a Service</button>
    </div>
  </div>
</template>

<script setup>
// You can add button event handlers or functionality here if needed
</script>

<style scoped>
.about-us-container {

  margin: 0 auto;
  padding: 20px;
  background-color: #fff5e1; /* Light gold background */
  border: 2px solid #d4af37; /* Gold border */
  border-radius: 8px;
  text-align: center;
}

.about-us-title {
  font-size: 32px;
  color: #b22222; /* Dark red color */
  margin-bottom: 15px;
}

.about-us-description {
  font-size: 18px;
  color: #333;
  margin-bottom: 20px;
}

.button-container {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 20px;
}

.action-button {
  padding: 10px 20px;
  font-size: 16px;
  font-weight: bold;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.call-us {
  background-color: #b22222; /* Red button */
  color: white;
}

.call-us:hover {
  background-color: #8b0000; /* Darker red on hover */
}

.contact-us {
  background-color: #d4af37; /* Gold button */
  color: white;
}

.contact-us:hover {
  background-color: #b8860b; /* Darker gold on hover */
}

.schedule-service {
  background-color: #b22222; /* Red button */
  color: white;
}

.schedule-service:hover {
  background-color: #8b0000; /* Darker red on hover */
}
</style>
