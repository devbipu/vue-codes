<template>
  <div id="app">
    <div class="buttonsWrapper">
      <button @click="activeTab = 'TabA'">Tab A</button>
      <button @click="activeTab = 'TabB'">Tab B</button>
      <button @click="activeTab = 'TabC'">Tab C</button>
    </div>
    <div class="tab_wrapper">
      <keep-alive>
        <component :is='activeTab'/>
      </keep-alive>
    </div>
    

    <!-- div class="tab_wrapper">
      <tabA v-if="activeTab === 'TabA'" />
      <tabB v-if="activeTab === 'TabB'" />
      <tabC v-if="activeTab === 'TabC'" />
    </div> -->
   

  </div>
</template>

<script>
  // import HelloWorld from './components/HelloWorld.vue'
  import TabA from './components/tabA.vue'
  import TabB from './components/tabB.vue'
  import TabC from './components/tabC.vue'
  export default {
    name: 'MainAppFile',
    data () {
      return{
        activeTab: "TabA",
      }
    },
    components: {
      TabA,
      TabB,
      TabC
    },
  }
</script>

<style>



  /*Custom css start*/
  .tab_wrapper {
    display: flex;
    justify-content: center;
    border: 1px solid black;
    padding: 20px 0px;
  }

  .buttonsWrapper{
    text-align: center;
  }















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
