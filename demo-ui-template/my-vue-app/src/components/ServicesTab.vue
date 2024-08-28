<template>
  <div class="services-tab">
    <table cellspacing="5" cellpadding="0" width="100%" border="0">
      <tr>
        <td align="center" valign="top" class="txtFAQ_Q">
          At Dent Busters, LLC, customer service is our top priority. That's why we proudly offer:
          <ul>
            <li class="txt3">Free Estimates</li>
            <li class="txt3">Same Day Service</li>
            <li class="txt3">Two Convenient Locations</li>
            <li class="txt3">Satisfaction Guaranteed or Your Money Back</li>
          </ul>
          
          <table cellspacing="5" cellpadding="0" border="0">
            <tr v-for="(link, index) in links" :key="index">
              <td valign="top" align="left" class="txt">
                <b>{{ link.title }}</b>
                {{ link.description }}
              </td>
            </tr>
          </table>
        </td>
        <td align="left" valign="top" width="200px">
          <img alt="Dent Repair" src="../assets/images/Services_Dent_Before.jpg" width="200px" border="0" />
          <img alt="Dent Repair" src="../assets/images/Services_Dent_After.jpg" width="200px" border="0" />
        </td>
      </tr>
      <tr>
        <td align="center" valign="top" class="txtFAQ_Q" colspan="2">
          Come to Dent Busters, LLC, today for an amazing alternative to time-consuming and costly body work.
          Our exclusive paintless process makes dings and dents disappear without the use of sanding, body fillers or paint
          at a cost far below that of regular body work. Our special process helps preserve your car's worth by retaining its
          original factory finish. Now mismatched paint or overspray won't take away from your car's value and appearance at trade-in time.
          Our process works best for parking lot door dings and hail damage where the factory paint has not been harmed.
        </td>
      </tr>
      <tr>
        <td align="left" valign="top" colspan="2">
          <!-- Empty content area -->
        </td>
      </tr>
    </table>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Sample data to simulate what the ASP.NET Repeater would fetch from a database or server
const links = ref([
  { title: 'Fast Service', description: 'We offer the fastest service available with quality that cannot be beat.' },
  { title: 'Affordable Prices', description: 'Our prices are affordable and transparent with no hidden costs.' },
  // Add more items as needed
]);
</script>

<style scoped>
.services-tab {
  padding: 20px;
  font-family: Arial, sans-serif;
}

.txtFAQ_Q {
  margin-top: 10px;
  font-size: 16px;
  color: #333;
}

.txt3 {
  font-size: 14px;
  margin-top: 5px;
}

img {
  display: block;
  margin: 10px 0;
}
</style>
