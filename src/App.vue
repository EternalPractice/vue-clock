<template>
  <div id="app">
    <Clock />
  </div>
</template>

<script>
import Clock from './components/Clock.vue';

export default {
  name: 'app',
  components: {
    Clock
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  background-color: black;
  height: 100vh;
  width: 100vw;
  display: grid;
  place-items: center;
}
</style>
