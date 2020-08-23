<template>
    <div>
        <h1>{{this.headerText}}</h1>
        <div>
            <img v-bind:src="this.imageUrl" />
        </div>
        <p>{{this.bodyText}}</p>
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'Slide',
  props: {
    headerText: String,
    bodyText: String,
    imageUrl: String
  }
}
</script>

<style>
</style>
