<template>
  <div id="app">
    <div class="ui inverted segment">
      <div class="ui inverted secondary pointing menu">
        <a class="active item">
          Home
        </a>
        <a class="item" :href="contactLink">
          Contact
        </a>
        <a class="item">
          Friends
        </a>
      </div>
    </div>

    <router-view/>

  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      contactLink: '/contact'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 2em;
  margin-top: 0;
}
</style>
