<script setup lang="ts">
import type { LinkButtonsProps } from '../types/';
import LinkButton from './LinkButton.vue';

defineProps<LinkButtonsProps>();
</script>

<template>
  <ul class="linkbuttons">
    <li v-for="socialButton in buttons">
      <LinkButton v-bind="socialButton" />
    </li>
  </ul>
</template>

<style scoped>
.linkbuttons {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 0;
  margin: 0;
  list-style: none;
  margin-top: 30px;
}

@media screen and (min-width: 768px) {
  .linkbuttons {
    justify-content: flex-start;
  }
}
</style>
