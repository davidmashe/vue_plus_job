<template>
  <div>
    <span>One</span>
    <Slide name="Slide" headerText="'sup braaah'" bodyText="yo yoyo" imageUrl="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" />
  </div>
</template>

<script>
import Slide from './Slide.vue';

export default {
  name: 'SlideOne',
  components: {
    Slide
  }
}
</script>

<style scoped>
</style>
