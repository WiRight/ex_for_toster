<template>
  <div id="app">
    <div>
      <button @click="toWiRight">
        Load WiRight component
      </button>
      <button @click="toHelloWorld">
        Load HelloWorld component
      </button>
    </div>
    <transition name="fade" appear>
      <router-view/>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    toWiRight: function () {
      this.$router.replace('/pageWiRight')
    },
    toHelloWorld: function () {
      this.$router.replace('/')
    }
  }
}
</script>

<style>
#app {
  border: 1px solid blue;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .3s ease;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
