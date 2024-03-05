<template>
  <div class="text-componenet">
    <h1>{{ title }}</h1>
    <div class="para" v-html="para"></div>
  </div>
</template>

<script>
export default {
  name: 'TextComponenet',
  props: {
    title: String,
    para: String,
  },
}
</script>

<style scoped>
.text-componenet {
  max-width: 718px;
  margin: 0 auto;
  padding-top: 110px;
}
.text-componenet > h1 {
  opacity: 1;
  color: #0e3757;
  font-family: '';
  font-size: 50px;
  font-weight: 400;
  letter-spacing: 0px;
  text-align: center;
  margin: 0;
  padding-bottom: 10px;
}
.text-componenet > .para {
  opacity: 1;
  color: #8d9ca8;
  font-family: '';
  font-size: 24px;
  font-weight: 400;
  letter-spacing: 0px;
  text-align: center;
  line-height: 36px;
  margin: 0;
}
@media only screen and (max-width: 630px) {
  .text-componenet {
    padding: 30px 15px 0 15px;
  }
  .text-componenet > h1 {
    font-size: 32px;
    line-height: 40px;
  }
  .text-componenet > .para {
    font-size: 20px;
    font-weight: 400;
    line-height: 30px;
  }
}
</style>
