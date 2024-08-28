<!-- BusinessHours.vue -->
<template>
    <div class="business-hours-container">
      <table class="business-hours-table" cellspacing="5" cellpadding="0" width="100%" border="0">
        <tr>
          <td class="txtFAQ_Q" width="100%" height="450px">
            <table cellspacing="15" cellpadding="0" width="300" border="0">
              <tr v-for="(hour, index) in businessHours" :key="index">
                <td align="right">{{ hour.day }}</td>
                <td align="center" valign="middle">{{ hour.time }}</td>
              </tr>
            </table>
          </td>
          <td valign="top" align="right">
            <img
              alt="Dent Busters Paintless"
              src="../assets/images/Texaco_Service_Station_BusinessHours.JPG"
              width="200"
              border="0"
            />
          </td>
        </tr>
      </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  // Define business hours
  const businessHours = ref([
    { day: 'Monday', time: '9:00 AM - 5:00 PM' },
    { day: 'Tuesday', time: '9:00 AM - 5:00 PM' },
    { day: 'Wednesday', time: '9:00 AM - 5:00 PM' },
    { day: 'Thursday', time: '9:00 AM - 5:00 PM' },
    { day: 'Friday', time: '9:00 AM - 5:00 PM' },
    { day: 'Saturday', time: '9:00 AM - 1:00 PM' },
    { day: 'Sunday', time: 'Closed' },
  ]);
  </script>
  
  <style scoped>
  .business-hours-container {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 20px;
  }
  
  .business-hours-table {
    width: 100%;
    border-spacing: 5px;
  }
  
  .txtFAQ_Q {
    font-size: 16px;
    line-height: 1.5;
  }
  
  img {
    margin-top: 20px;
  }
  </style>
  