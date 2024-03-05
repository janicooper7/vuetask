<template>
  <NavigationComponent />
  <TextComponent
    title="We Do Awesome Things"
    para="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  />
  <ImageComponent />
  <RecallBannerComponent
    title="Lorem ipsum dolor sit amet, consectetur adipiscing elit!"
  />
  <TextComponent
    title="We Do Really Awesome Things"
    para="<p>Lorem ipsum dolor sit amet, <a href='/#''>link</a> consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>"
  />
  <CardComponent />
  <ReviewComponent />
  <TextComponent
    title="Contact About Awesomeness"
    para="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
  />
  <FormComponent />
  <FooterComponent />
</template>

<script>
import NavigationComponent from './components/NavigationComponent'
import TextComponent from './components/TextComponent'
import ImageComponent from './components/ImageComponent'
import RecallBannerComponent from './components/RecallBannerComponent'
import CardComponent from './components/CardComponent'
import ReviewComponent from './components/ReviewComponent'
import FormComponent from './components/FormComponent'
import FooterComponent from './components/FooterComponent'

export default {
  name: 'App',
  components: {
    NavigationComponent,
    TextComponent,
    ImageComponent,
    RecallBannerComponent,
    CardComponent,
    ReviewComponent,
    FormComponent,
    FooterComponent,
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');
html,
body {
  font-family: 'Roboto', sans-serif;
}
#app {
  font-family: 'Roboto', sans-serif;
}
* {
  box-sizing: border-box;
}
body {
  margin: 0;
}
</style>
