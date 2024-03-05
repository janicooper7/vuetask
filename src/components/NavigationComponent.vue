<template>
  <nav class="nav">
    <input type="checkbox" id="nav-check" />
    <div class="nav-header">
      <img src="@/assets/logo/primary.png" alt="Logo Image" />
    </div>
    <div class="nav-btn">
      <label for="nav-check">
        <span></span>
        <span></span>
        <span></span>
      </label>
    </div>

    <ul class="nav-list">
      <li><a href="#">About Us</a></li>
      <li><a href="#">About You</a></li>
      <li><a href="#">Portfolio</a></li>
      <li class="active"><a href="#">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavigationComponent',
}
</script>

<style scoped>
.nav {
  width: 100%;
  display: flex;
  align-items: center;
  max-width: 1087px;
  height: 50px;
  margin: 10px auto 0;
}
.nav > .nav-header {
  flex: 0.95;
  padding-left: 1rem;
}
.nav > .nav-header > img {
  width: 120px;
}
.nav > .nav-header > .nav-title {
  font-size: 22px;
  color: #000;
}
.nav > .nav-list {
  display: flex;
  gap: 1rem;
}
.nav > .nav-list > li {
  list-style-type: none;
  padding: 10px;
  border-radius: 5px;
  text-align: center;
}
.nav > .nav-list > .active {
  opacity: 1;
  background-color: #f56a75;
  padding: 10px 30px;
}
.nav > .nav-list > .active > a {
  color: #fff;
}
.nav > .nav-list > li a {
  text-decoration: none;
  color: #000;
  cursor: pointer;
  font-size: 18px;
}
.nav > #nav-check {
  display: none;
}
@media only screen and (max-width: 630px) {
  .nav {
    padding: 1rem;
  }
  .nav > .nav-header {
    padding-left: 0;
  }
  .nav > .nav-header > img {
    width: 75px;
    height: 32px;
  }
  .nav > .nav-btn {
    display: inline-block;
    position: absolute;
    right: 10px;
    top: 0;
    padding-top: 0.2rem;
  }
  .nav > .nav-btn > label {
    display: inline-block;
    width: 50px;
    height: 50px;
    padding: 13px;
  }
  .nav > .nav-btn > label > span {
    display: block;
    width: 25px;
    height: 10px;
    border-top: 2px solid #000;
  }
  .nav > .nav-list {
    position: absolute;
    display: flex;
    flex-direction: column;
    gap: 0;
    width: 100%;
    background-color: #0e3757;
    height: 0;
    transition: all 0.3s ease-in;
    top: 40px;
    right: 0;
    overflow: hidden;
    max-width: 258px;
    padding: 0 30px;
  }
  .nav > .nav-list > li {
    width: 100%;
    margin-top: 1.5rem;
    padding: 0;
  }
  .nav > .nav-list > li > a {
    color: #fff;
  }
  .nav > #nav-check:checked ~ .nav-list {
    height: calc(100vh - 50px);
  }
}
</style>
