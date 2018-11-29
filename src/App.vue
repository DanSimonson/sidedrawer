<template>
  <div id="app">
    <div class='test' v-on:click="active = !active" v-bind:class={active:active}>
      <svg width="30" height="30">
        <path d="M0,5 30,5" stroke="#111" stroke-width="5" />
        <path d="M0,14 30,14" stroke="#111" stroke-width="5" />
        <path d="M0,23 30,23" stroke="#111" stroke-width="5" />
      </svg>
    </div>

    <!--<router-view/> -->
  </div>
</template>

<script>
  export default {
    data() {
      return {
        active: false
      }
    }
  }
</script>

<style scoped>
  .test {
    border: 5px solid red;
    width: 0;
    height: 95vh;

  }

  .active {
    background-color: green;
    width: 250px;
  }

  #app {
    /*font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;*/
  }

  /*#nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }*/
</style>