<template>
  <div v-show="isShow ? true : false">
    <a class="overlay" href="" @click="isShow = false"></a>
    <div class="modal">
      <div class="modal-content">
        {{content}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',

  props: {
    content: String,
    isShow: Boolean,
  },
}
</script>

<style scoped>
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.5)
  }
  .modal {
    max-width: 600px;
    width: 100%;
    background-color: #fafafa;
    border: 1px solid #eaeaea;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 10;
    min-height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

</style>
