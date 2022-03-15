<template>
  <div>
    <h1>{{ text }}</h1>
    <Navbar />
    <p :class="myClass">Este párrafo cambia de color</p>
    <button @click="button">Haz click aqui</button>
  </div>
</template>

<script>
import Navbar from './components/Navbar';
export default {
  name: 'App',
  data () {
    return{
     text: 'Bienvenido a mi página',
     myClass: 'red'
    }
  },
  components: {
    Navbar
  },

  methods:{
    button  (){
      this.myClass = 'green';
    }
  }
}
</script>

<style>
  .red {
    color: red;
  }

  .green {
    color: green;
  }
</style>
