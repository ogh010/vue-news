<template>
  <div id="app">
    <tool-bar></tool-bar>
      <router-view></router-view>
    
  </div>
</template>

<script>
import ToolBar from './components/ToolBar.vue'

export default {
  methods: {
    fectData(){
      console.log('hello');
    }
  },
  components:{
    ToolBar,
  }
}
</script>
<style>
*{padding: 0;margin: 0;}
a{text-decoration: none; color: #333;}
a:hover{color:tan; border-bottom: 1px solid tan;}
</style>
