<template>
  <header class="header">
    <div class="header-content">
      <div class="image-wrapper">
        <img alt="Dent Busters" src="../assets/images/Dent_Busters_Paintless_Header.gif" class="header-image" />
      </div>
      <div class="image-wrapper">
        <img alt="Dent Busters" src="../assets/images/Dent_Busters_Paintless_Header_Sub.gif" class="header-sub-image" />
      </div>
    </div>
  </header>
</template>

<script setup>
// No script is required for this static content component
</script>

<style scoped>
.header {
  background: linear-gradient(to right, #d32f2f, #fbc02d); /* Red to gold gradient */
  padding: 20px 0;
  text-align: center;
  position: relative;
  overflow: hidden; /* Ensures that gradients cover the content */
  border-radius: 8px;
}

.header-content {
  max-width: 950px;
  margin: 0 auto;
  position: relative;
  z-index: 1; /* Ensures content is above the gradient overlay */
}

.image-wrapper {
  position: relative;
  display: inline-block;
}

.header-image, .header-sub-image {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  opacity: 0.8; /* Adjust opacity for transparency */
  position: relative;
  z-index: 1; /* Ensures images are above the gradient overlay */
  border-radius: 8px;
}

.header-image::before, .header-sub-image::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, 0.5) 100%);
  pointer-events: none;
  z-index: 2; /* Overlay above the image */
  opacity: 0.8; /* Adjust overlay opacity */
  border-radius: 8px;
}
</style>
