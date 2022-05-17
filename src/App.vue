<template>
  <div id="app">

   <HelloWorld>
     <template v-slot:default='datasKey'>
       <p>
         First name: {{datasKey.fname}}
        Last name: {{datasKey.lname}}
       </p>
     </template>
   </HelloWorld>
    <HelloWorld>
     <template v-slot:default='datasKey'>
       <p>
          First name: {{datasKey.fname}}
       </p>
     </template>
   </HelloWorld>

  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  export default {
    name: 'MainAppFile',
    data () {
      return{
        names: "",
      }
    },
    components: {
      HelloWorld,
    },
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /*text-align: center;*/
    color: #2c3e50;
    margin-top: 60px;
  }
  img{
    width: 100%;
  }


  .underline{
    text-decoration: underline;
  }
  .green{
    color: green;
  }
  .red{
    color: red;
  }


  .header_transparent .main-sticky-header:not(.sticky-header) section.elementor-element:not(.no-transparent) {
    background-color: #fff !important;
  }

  .header_transparent .maiWn-sticky-header:not(.topheader){
    background-color: #fff !important;
  }






</style>
