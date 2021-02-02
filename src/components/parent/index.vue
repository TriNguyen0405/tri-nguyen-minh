<template>
   <div>
      <h2>{{title}}</h2>
      <div>
         <Modal content="Content button 111111 !!!" v-show="isShow = isShow1 " />   
         <button @click="isShow1 = true">Button 1</button>      
      </div>

      <div>
         <Modal content="Content button 222222 !!!" v-show="isShow = isShow2" />   
         <button @click="isShow2 = true">Button 2</button>      
      </div>

      <div>
         <Modal content="Content button 333333 !!!" v-show="isShow = isShow3" />   
         <button @click="isShow3 = true">Button 13</button>      
      </div>
   </div>
</template>


<script>
import Modal from './../modal/index.vue'

export default {
   name: 'Parent',

   props: {
      title: String,
   },

   data() {
      return {
         isShow1: false,
         isShow2: false,
         isShow3: false,
      }
   },

   components: {
      Modal
   }
}
</script>


<style scoped>

</style>