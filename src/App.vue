<template>
 <h1>{{title}}</h1>
 <p>Welcome...</p>
<teleport to=".modals" v-if="showModal">
  <Modal  theme="sale" @close="changeModal">
      <h1>OpenCode Giveaway !</h1>
      <p>Grab the course for half price</p>
      <template v-slot:links>
        <a href="#">Sign up</a>
        <a href="#">more info</a>
      </template>
    </Modal>
</teleport>

<teleport to=".modals" v-if="showModalTwo">
  <Modal  theme="sale" @close="changeModalTwo">
      <h1>Sign up for news !</h1>
      <p>Dont lose any</p>
      
    </Modal>
</teleport>

<button @click="changeModal">show Modal</button>
<button @click="changeModalTwo">show Modal Two</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
 data(){
  return{
    title: 'My vue APP',
    showModal: false,
    showModalTwo:false,
  }
 },
 methods: {
  changeModal(){
    this.showModal= !this.showModal
  },
  changeModalTwo(){
    this.showModalTwo= !this.showModalTwo
  }
 }
}
</script>

<style>
#app, .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  color: blueviolet;
}
</style>
