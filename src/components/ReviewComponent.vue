<template>
  <div class="review-component">
    <img src="@/assets/generic/speach-marks.png" alt="Speach marks" />
    <div class="review-wrapper">
      <p class="review">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
      <p class="author">Roy Barber - Dotcentric</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ReviewComponenet',
}
</script>

<style scoped>
.review-component {
  max-width: 1080px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin-top: 100px;
  border-top: 2px solid #8d9ca8;
  border-bottom: 2px solid #8d9ca8;
  padding: 62px 92px;
}
.review-component > .review-wrapper {
  padding-left: 43px;
}
.review-component > img {
  width: 50px;
  height: 33px;
  margin-top: 10px;
}
.review-component > .review-wrapper > .review {
  opacity: 1;
  color: #0e3757;
  font-size: 28px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 42px;
  margin: 0;
}
.review-component > .review-wrapper > .author {
  opacity: 1;
  color: #8d9ca8;
  font-size: 18px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 30px;
  margin-bottom: 0;
}
@media only screen and (max-width: 630px) {
  .review-component {
    margin: 40px 15px 0 15px;
    padding: 30px 0;
  }
  .review-component > img {
    width: 30px;
    height: 20px;
  }
  .review-component > .review-wrapper {
    padding-left: 18px;
  }
  .review-component > .review-wrapper > .review {
    font-size: 22px;
    line-height: 36px;
  }
  .review-component > .review-wrapper > .author {
    font-size: 18px;
    line-height: 30px;
  }
}
</style>
