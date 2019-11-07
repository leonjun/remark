<template>
  <div id="app">
    
    
    <router-view/>
  </div>
</template>



<script>
//import "@/assets/live2d/css/live2d.css";
//import "@/assets/live2d/js/live2d.js";
export default {
  name: 'App',
//   created () {
  
//     window.L2Dwidget.init({
//       pluginRootPath: '/static/live2dw/',
//       pluginJsPath: 'lib/',
//       pluginModelPath: 'live2d-widget-model-koharu/assets/',
//       tagMode: false,
//       debug: false,
//       model: { jsonPath: '/static/live2dw/live2d-widget-model-koharu/assets/koharu.model.json' },
//       display: { position: 'left', width: 150, height: 300 },
//       mobile: { show: true },
//       log: false
//     })
  
// }
  // created(){
   
  //   loadlive2d("live2d", "@/assets/live2d/model/tia/model.json");
  // }
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
</style>
