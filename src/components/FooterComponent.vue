<template>
  <footer>
    <div class="footer-content">
      <p>
        © 2021 <span class="orange-font">Dotcentric</span> Code Test - All
        rights reserved - Call <a href="tel:01234 432 123">01234 432 123</a>
      </p>
      <img src="@/assets/logo/secondary.png" alt="Logo Image" />
    </div>
  </footer>
</template>
<script>
export default {
  name: 'FooterComponent',
}
</script>
<style scoped>
footer {
  margin-top: 125px;
  background-color: #0e3757;
  padding: 25px 15px;
}
.footer-content {
  max-width: 1080px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.footer-content > p {
  opacity: 1;
  color: #eee;
  font-size: 20px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 10px;
}
.footer-content > p > a {
  color: #eee;
  text-decoration: none;
}
.footer-content > p > .orange-font {
  color: #f56a75;
}
.footer-content > img {
  width: 120px;
  height: auto;
}
@media only screen and (max-width: 630px) {
  footer {
    margin-top: 40px;
    padding: 40px 15px;
  }
  .footer-content {
    display: flex;
    flex-direction: column-reverse;
    text-align: center;
  }
  .footer-content > p {
    font-size: 18px;
    line-height: 27px;
    margin: 30px 0 0 0;
  }
  .footer-content > img {
    margin: 0 auto;
  }
}
</style>
