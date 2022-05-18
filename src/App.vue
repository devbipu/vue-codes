<template>
  <div id="app">
    <button @click='activeTab = !activeTab'>Show</button>
    <TabA v-if='activeTab === true'/>
  </div>
</template>

<script>
  // import HelloWorld from './components/HelloWorld.vue'
  import TabA from './components/tabA.vue'
  // import TabB from './components/tabB.vue'
  // import TabC from './components/tabC.vue'
  // import PostList from './components/posts.vue';


  export default {
    name: 'MainAppFile',
    data () {
      return{
        activeTab: true,
      }
    },
    components: {
      TabA,
    },
    beforeCreate() {
      console.log('Parents beforeCreate')
    },
    created() {
      console.log('Parents created')
    },
    beforeMount() {
      console.log('Parents beforeMount')
    },
    mounted() {
      console.log('Parents mounted')
    },
    beforeUpdate() {
      console.log('Parents beforeUpdate')
    },
    updated() {
      console.log('Parents Update')
    },
    beforeUnmount() {
      console.log('Parents beforeUnmount')
    },
    unmounted(){
      console.log('Parents unmouned')
    }
  }
</script>

<style>



  /*Custom css start*/
  













  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
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
  button {
    background: #ededed;
    border: 1px solid #dbdbdb;
    padding: 10px 30px;
    border-radius: 3px;
  }



</style>
