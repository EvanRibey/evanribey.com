<script setup lang="ts">
import classnames from 'classnames';
import type { LinkButtonProps } from '../types/';

defineProps<LinkButtonProps>();
</script>

<template>
<a
  target="_blank"
  :href="href as string"
  :title="title as string"
  class="linkbutton"
>
  <i :class="classnames('linkbutton-icon', 'fab', fontAwesomeClass)"></i>
</a>
</template>

<style scoped>
.linkbutton {
  text-decoration: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  border: 1px solid #2e2e2e;
  transition: background-color 0.3s;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  margin: 0 7px;
  font-size: 2.24rem;
}

.linkbutton-icon {
  color: #0f0f0f;
  transition: color 0.3s;
}

.linkbutton:first-of-type {
  margin-left: 4px;
}

.linkbutton:hover {
  background-color: #0f0f0f;
}

.linkbutton:hover .linkbutton-icon {
  color: #fcfcfc;
}

@media screen and (max-width: 768px) {
  .link {
    margin-left: 7px;
  }
}
</style>
