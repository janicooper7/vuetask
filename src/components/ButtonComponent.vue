<template>
  <div class="cta">
    <button @click="say(title)">{{ title }}</button>
  </div>
</template>

<script>
export default {
  name: 'ButtonComponent',
  props: {
    title: String,
  },
  methods: {
    say: function (message) {
      alert(message)
    },
  },
}
</script>

<style>
.cta > button {
  opacity: 1;
  background-color: #0e3757;
  width: 120px;
  height: 50px;
  color: #fff;
  border-radius: 5px;
  border: 0;
}
.cta > button:hover {
  cursor: pointer;
}
@media only screen and (max-width: 630px) {
  .cta > button {
    width: 100%;
    margin-top: 40px;
  }
}
</style>
