<template>
  <div id="app">
    <img src="./assets/logo.png">
    <p>You can display the Tippy tooltip by hover the text below!</p>
    <p ref="tippy">
      Tippy.js
    </p>
  </div>
</template>

<script>
import tippy from 'tippy.js';

export default {
  name: 'App',

  data () {
    return {
      tippy: 'test',
    }
  },

  mounted() {
    console.log(`{}.toString.call(Element): ${{}.toString.call(this.$refs.tippy)}`);
    tippy(this.$refs.tippy, {
      content: 'Hello Vue World!',
    });
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
