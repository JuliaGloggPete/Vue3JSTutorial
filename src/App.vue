<template>
<h1>{{title}}</h1>
<p>Welcome ... </p>
<teleport to=".modals" v-if="showModal">

  <Modal theme="sale" @close="toggleModal" >
<template v-slot:links>
<a href="#">sign up now</a>
<a href="#">more info</a>

</template>
<h1>Julia</h1>
<p>start to focus now</p>

</Modal>
</teleport>
<div v-if="showModalTwo">
<Modal theme="heart" @close="toggleModalTwo">




  <h1>Something </h1>


</Modal>
</div>

<button @click="toggleModal" >open modal</button>
<button @click="toggleModalTwo" >open modal 2</button>

</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal},
  data(){
    return{
      title:'NetNinja Tutorial',
      showModal: false,
      showModalTwo: false

    }
  },

  methods:{
    toggleModal(){
      this.showModal = !this.showModal
    },
    toggleModalTwo(){
      this.showModalTwo = !this.showModalTwo
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
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;

}
</style>
