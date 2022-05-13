<template>
  <div id="app">
    <button @click='popup = true'>Show popup</button>
    <HelloWorld v-show='popup' @close="popuphandeler" title='This is title' :postLike='30' :isPublish='true'/>
    <h3>App components username: {{ fname }}</h3>
    <compoa1 :names='fname'/>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import compoa1 from './components/compoa1.vue'
  export default {
    name: 'devbipu',
    data () {
      return{
        fname: "Biplob",
        lname: "Shaha",
        popup: false,
      }
    },
    components: {
      HelloWorld,
      compoa1,
    },
    provide() {
      return {
        username: this.fname
      }
    },
    methods: {
      popuphandeler(name){
        this.popup = false;
        console.log("Message", name)
      }
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
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
