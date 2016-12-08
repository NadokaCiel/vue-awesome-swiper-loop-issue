<template>
  <div id="app">
    <div class="main-content">
      <home></home>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'
export default {
  name: 'app',
  data() {
    return {
    }
  },
  created: function() {
    let vm = this;
  },
  components: {
    Home,
  }
}
</script>

<style>
#app {
  font-family: "Microsoft YaHei", "Verdana", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: relative;
  min-width: 480px;
  margin: 0;
  font-size: 12px;
}
.main-content {
}
</style>