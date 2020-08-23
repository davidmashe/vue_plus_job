<template>
  <div id="app">
    <div :is="this.router[this.selectedIndex]" />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import SlideOne from './components/slides/SlideOne.vue';
import SlideTwo from './components/slides/SlideTwo.vue';
import SlideThree from './components/slides/SlideThree.vue';
// import SlideFour from './components/slides/SlideFour.vue';
// import SlideFive from './components/slides/SlideFive.vue';
// import SlideSix from './components/slides/SlideSix.vue';
// import SlideSeven from './components/slides/SlideSeven.vue';

export default {
  name: 'App',
  components: {
    SlideOne,
    SlideTwo,
    SlideThree,
    // SlideFour,
    // SlideFive,
    // SlideSix,
    // SlideSeven
  },
  data: function() {
    return {
      router: [
        SlideOne,
        SlideTwo,
        SlideThree,
        // SlideFour,
        // SlideFive,
        // SlideSix,
        // SlideSeven
      ],
      selectedIndex: 0
    }; 
  },
  created: function() {
    document.addEventListener('keydown', ({ keyCode }) => {
      const { selectedIndex, router } = this;
      const right = 39;
      const left = 37;
      const isRight = keyCode === right;
      const isLeft = keyCode === left;
      const lastSlide = router.length - 1;

      if (isRight && selectedIndex < lastSlide) {
        console.log('forward!');
        this.selectedIndex = selectedIndex + 1;
      } else if (isLeft && this.selectedIndex > 0) {
        console.log('back!');
        this.selectedIndex = selectedIndex - 1;
      }
    });
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
