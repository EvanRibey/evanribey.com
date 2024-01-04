<script setup lang="ts">
import type { LinkButtonProps } from '../types/';
import LinkButtons from './LinkButtons.vue';

const buttons: LinkButtonProps[] = [
  {
    title: 'LinkedIn Profile',
    href: 'https://www.linkedin.com/in/evanribey/',
    fontAwesomeClass: 'fa-linkedin-in',
  },
  {
    title: 'Github Profile',
    href: 'https://github.com/EvanRibey',
    fontAwesomeClass: 'fa-github',
  },
];
</script>

<template>
<div class="homeinformation">
  <h1 class="homeinformation-title">Evan Ribey</h1>
  <hr class="homeinformation-keyline">
  <p class="homeinformation-summary">Full-Stack Developer, looking to collaborate and focus on client needs.</p>
  <p class="homeinformation-summary">I like solving puzzles while enjoying a nice cup of coffee.</p>
  <LinkButtons :buttons="buttons" />
</div>
</template>

<style scoped>
.homeinformation {
  display: flex;
  justify-content: center;
  flex-direction: column;
  min-width: 200px;
  align-items: center;
  width: 90vw;
}

.homeinformation-title {
  font: normal 600 4.4rem var(--cinzel);
  letter-spacing: 2px;
  color: #0f0f0f;

  margin: 0 0 15px;
  padding-left: 5px;
}

.homeinformation-keyline {
  background-color: #d1d1d1;
  height: 1px;
  width: 100%;
  margin-bottom: 20px;
}

.homeinformation-summary {
  font: normal 300 1.9rem var(--nunito);
  letter-spacing: 1px;
  text-align: center;
  line-height: 1.5;

  padding-left: 0;
  margin: 6px 0;
  max-width: 27.7rem;
}

.homeinformation-link {
  font-weight: 300;
  text-decoration: none;
  color: #0f0f0f;
  position: relative;
}

.homeinformation-link::after {
  content: '';
  position: absolute;
  bottom: 3px;
  left: 0;
  width: 100%;
  background-color: currentColor;
  opacity: 0;
  height: 1px;
  transition: bottom 0.2s, opacity 0.2s;
}

.homeinformation-link:hover::after {
  opacity: 1;
  bottom: 0px;
}

@media screen and (min-width: 768px) {
  .homeinformation {
    align-items: flex-start;
    width: 35vw;
  }

  .homeinformation-summary {
    padding-left: 5px;
    text-align: left;
    max-width: none;
  }
}
</style>
