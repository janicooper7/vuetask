<template>
  <div class="recall-banner">
    <div class="recall-wrapper">
      <div class="text-area">
        <p>{{ title }}</p>
      </div>
      <ButtonComponent title="Call Now" />
    </div>
  </div>
</template>

<script>
import ButtonComponent from './ButtonComponent'

export default {
  name: 'RecallBannerComponent',
  components: {
    ButtonComponent,
  },
  props: {
    title: String,
  },
}
</script>

<style scoped>
.recall-banner {
  background-color: #f56a75;
}
.recall-banner > .recall-wrapper {
  max-width: 1100px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 auto;
  padding: 30px 15px;
}
.recall-banner > .recall-wrapper > .text-area > p {
  margin: 0;
  opacity: 1;
  color: rgba(255, 255, 255, 1);
  font-size: 28px;
  font-weight: 400;
  letter-spacing: 0px;
  text-align: left;
  line-height: 42px;
}
@media only screen and (max-width: 630px) {
  .recall-banner > .recall-wrapper {
    flex-direction: column;
    width: 320px;
    padding: 30px 15px 30px 15px;
  }
  .recall-banner > .recall-wrapper > .text-area > p {
    font-size: 22px;
    font-weight: 400;
    line-height: 36px;
    text-align: center;
  }
}
</style>
