<template>
  <Container />
</template>

<script>
import Container from './components/Container.vue'

export default {
  name: 'App',
  components: {
    Container
  }
}
</script>

<style>
body {
  background-color: rgb(235, 235, 235);
  display: flex;
  justify-content: center;
}
#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 50px;
  background-color: rgb(240, 240, 240);
  width: 400px;
  box-shadow: 0px 0px 15px 0px rgba(200,200,200,0.5);
  letter-spacing: -1px;
}
</style>
