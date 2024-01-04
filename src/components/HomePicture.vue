<template>
  <div class="homepicture">
    <img class="homepicture" src="../assets/Evan.jpg" alt="picture of man smiling" />
  </div>
</template>

<style>
.homepicture {
  width: 20vw;
  height: 20vw;
  min-width: 180px;
  min-height: 180px;
  border: 1px solid #2e2e2e;
  box-shadow: 0 1px 8px #999;
  border-radius: 50%;
  margin: 0 0 35px;
}

@media screen and (min-width: 768px) {
  .homepicture {
    min-width: 350px;
    min-height: 350px;
    margin: 0 35px 0 0;
  }
}
</style>
