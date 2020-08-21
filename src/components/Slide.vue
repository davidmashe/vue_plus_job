<template>
	slide
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data: function() {
    return {
    	router: [],
    	selectedIndex: 0
	};
  },
  created: function() {

  }
}
</script>

<style>
</style>
