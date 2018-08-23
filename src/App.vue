<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import Login from './components/Login'

export default {
  components: {
    Login
  }
}
</script>

<style>
  body {
    background-image: url(assets/bg-blur.jpg);
  }
</style>
