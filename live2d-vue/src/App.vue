<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>  -->
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {
  
  },
  created () {
  setTimeout(() => {
    window.L2Dwidget.init({
      pluginRootPath: 'static/live2dw/',
      pluginJsPath: 'lib/',
      pluginModelPath: 'live2d-widget-model-koharu/assets/',
      tagMode: false,
      debug: false,
      model: { jsonPath: '../static/live2dw/live2d-widget-model-koharu/assets/koharu.model.json' },
      display: { position: 'left', width: 150, height: 300 },
      mobile: { show: true },
      log: false
    })
  }, 1000)
},
  mounted() {
    // setTimeout(() => {
    //   window.L2Dwidget.init({
    //       pluginRootPath: 'live2dw/',
    //       pluginJsPath: 'lib/',
    //       pluginModelPath: 'live2d-widget-model-z16/assets/',
    //       tagMode: false,
    //       debug: false,
    //       model: { jsonPath: '../static/live2dw/live2d-widget-model-z16/assets/z16.model.json' },
    //       display: { position: 'right', width: 100, height: 200 },
    //       mobile: { show: true },
    //       log: false
    //       })
    // }, 1000)
  },
  data(){
    return{
      mdata: {
        name: "Epsilon2.1", // 模型名称
        model: "/api/assets/Epsilon2.1/Epsilon2.1.moc", // 模型文件地址
        textures: [
             "/api/assets/Epsilon2.1/Epsilon2.1.2048/texture_00.png", // 材质素材地址
        ]
    }
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
</style>
