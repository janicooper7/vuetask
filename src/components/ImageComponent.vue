<template>
  <div class="body-image">
    <img src="@/assets/generic/browser-image.png" alt="Browser Image" />
  </div>
</template>

<script>
export default {
  name: 'ImageComponent',
}
</script>

<style scoped>
.body-image {
  max-width: 914px;
  margin: 0 auto;
  padding-top: 100px;
}
.body-image > img {
  width: 100%;
  vertical-align: top;
}
@media only screen and (max-width: 630px) {
  .body-image {
    max-width: 300px;
    padding-top: 40px;
  }
}
</style>
