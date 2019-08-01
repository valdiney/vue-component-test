<template>
  <div id="app">
    <div class="container-fluid">
      {{quantidade}}
      <Menu v-on:incrementar="adicionarQuantidade"/>
      <Usuarios v-bind="{idCliente:quantidade}"/>
      
    </div>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Usuarios from "./components/Usuarios.vue"
import Menu from "./components/Menu.vue"

export default {
  name: 'app',
  components: {
    //HelloWorld
    Usuarios,
    Menu
  },

   data() {
        return {
            quantidade:19
        }
    },

  methods: {
    adicionarQuantidade() {
        this.quantidade++
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
