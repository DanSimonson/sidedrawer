<template>
  <div id="app">
    <div class='nav-bar' @click="active = !active" v-bind:class={active:active}>
      <transition name="fade">
        <svg v-if="!active" class='burger' width="30" height="30">
          <path d="M0,5 30,5" stroke="#111" stroke-width="5" />
          <path d="M0,14 30,14" stroke="#111" stroke-width="5" />
          <path d="M0,23 30,23" stroke="#111" stroke-width="5" />
        </svg>
      </transition>
      <a href="#" class="btn-close"><i class="fas fa-times"></i></a>
      <div id="side-menu" class="side-nav">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
      </div>
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
  .burger:hover {
    cursor: pointer;
  }

  .burger {
    top: 20px;
    right: 25px;
    position: fixed;
  }

  #app {
    position: relative;
  }

  .nav-bar {
    /*border: 5px solid red;*/
    position: absolute;
    width: 0;
    height: 95vh;
    top: 0;
    right: 0;
    position: fixed;
    z-index: 1;
    opacity: 0.9;
    overflow-x: hidden;
    padding-top: 60px;
    background-color: #BBDEFB;
    transition: .5s;

  }

  .nav-bar.active {
    background-color: #BBDEFB;
    width: calc(2px + 30%);
  }

  .side-nav {
    /*border: 5px solid black;*/
    display: flex;
    height: 40%;
    margin-top: 50px;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
  }

  .side-nav a {
    text-decoration: none;
  }

  .side-nav a:hover {
    color: #fff;
    text-decoration: none;
  }

  .nav-bar .btn-close {
    position: absolute;
    top: 0;
    left: 22px;
    font-size: 36px;
    /*
    right: 22px;
    margin-left: 50px;
    */
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity .5s;
    transition-delay: .5s;
  }

  .fade-enter,
  .fade-leave-to

  /* .fade-leave-active in <2.1.8 */
    {
    opacity: 0;
  }
</style>