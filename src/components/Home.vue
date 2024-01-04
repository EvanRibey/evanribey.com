<script setup lang="ts">
import HomePicture from './HomePicture.vue';
import HomeInformation from './HomeInformation.vue';
</script>

<template>
  <div class="home">
    <HomePicture />
    <HomeInformation />
  </div>
</template>



<style>
.home {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

@media screen and (min-width: 768px) {
  .home {
    flex-direction: row;
  }
}
</style>
