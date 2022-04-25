<template>
  <HomePage />
</template>

<script>
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    HomePage
  }
}
</script>

<style>
@font-face {
	font-family: 'Source Sans Pro';
	font-style: normal;
	font-display: auto;
	src: url('./assets/Source_Sans_Pro/SourceSansPro-Regular.ttf') format('truetype');
}
@font-face {
	font-family: 'Source Sans Pro Black';
	font-style: normal;
	font-display: auto;
	src: url('./assets/Source_Sans_Pro/SourceSansPro-Bold.ttf') format('truetype');
}
#app {
  font-family: 'Source Sans Pro', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  margin: 0;
  min-width: 960px;
  max-width: 100%;
  overflow-x: scroll;
}
</style>
