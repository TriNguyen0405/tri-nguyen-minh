<template>
  <div id="app">

    <div class="logo">
      <img alt="Vue logo" src="./assets/logo.png">
    </div>

    <div>
      <Modal content="Popup Vue js !!!" v-show="isShow"/>
      <button @click="isShow = true"> show popup </button>
    </div>

    <div>
      <ComponentParent title="Component Parent" />
    </div>

  </div>
</template>

<script>
import Modal from './components/modal/index.vue'
import ComponentParent from './components/parent/index.vue'

export default {
  name: 'App',

  data() {
    return {
      isShow: false,
    }
  },

  components: {
    Modal,
    ComponentParent
  }
}
</script>

<style>
  #app {
    text-align: center;
  }
  .logo {
    width: 100%;
  }
  
  button {
    margin: 20px 0;
  }
</style>
