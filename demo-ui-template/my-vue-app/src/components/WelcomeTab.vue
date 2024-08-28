<template>
  <div class="home-tab">
    <div class="content">
      <div class="text-section">
        <h1>25 Years of Dent Repair Expertise</h1>
        <h2>The Paintless Dent Removal Specialists</h2>
        <p class="description">
          Dent Busters, where we specialize in paintless dent removal for passenger vehicles
          in the Triangle area.
        </p>
        <ul>
          <li class="feature">Have unsightly parking lot dings decreased the value of your car?</li>
          <li class="feature">Do you need hail dents repaired, but you are worried about the cost?</li>
        </ul>
        <p class="description">
          Call Dent Busters today and learn about our paintless dent removal system. Our friendly
          and experienced technicians will restore your car's value and looks in just one day!
        </p>
      </div>
      <div class="image-section">
        <img alt="Dent Repair" src="../assets/images/Honda_cart_anime.gif" />
        <img alt="Dent Repair" src="../assets/images/Honda_golf_anime.gif" />
        <img alt="Dent Repair" src="../assets/images/Honda_hail_anime.gif" />
      </div>
    </div>
    <div class="additional-info">
      <ul>
        <li class="feature">
          Less costly than traditional repair, the Dent Busters system preserves your original
          paint finish.
        </li>
        <li class="feature">
          We make dents disappear without the use of sanding, body fillers, or paint at a
          cost far below that of regular body work.
        </li>
        <li class="feature">
          Our craftsmen have been trained in the art of paintless dent repair. We guarantee
          your complete satisfaction or your money back.
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
// No script is required for this static content component
</script>

<style scoped>
.home-tab {
  padding: 20px;
  font-family: Arial, sans-serif;
  background-color: #fff8e1; /* Light gold background */
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.text-section {
  width: 60%;
}

.image-section {
  width: 35%;
}

.text-section h1, .text-section h2 {
  color: #d32f2f; /* Dark red for headings */
}

.description {
  margin-top: 10px;
  font-size: 16px;
  color: #333;
}

.feature {
  font-size: 14px;
  margin-top: 5px;
  color: #d32f2f; /* Dark red for list items */
}

.image-section img {
  display: block;
  margin: 10px 0;
  width: 100%; /* Responsive image width */
}

.additional-info {
  margin-top: 20px;
}

.additional-info ul {
  list-style-type: disc;
  padding-left: 20px;
}
</style>
