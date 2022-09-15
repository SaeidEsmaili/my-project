<template>
 <h1>{{title}}</h1>
 

 <Modal />
</template>

<script>
import Modal from './components/Modal.vue'



export default {
  name: 'App',
  components: {Modal},
 data(){
  return{
    title: 'test for webpage'
  }
 },
 methods: {
  handleEvent(){
    console.log('test');
    console.log(this.$refs.name);
    this.$refs.name.classList.add('test')
  }
 }
}
</script>

<style>
#app {
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
