<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import axios from "axios";
//import jsonp from "jsonp";
export default {
  name: "App",
  components: {
    HelloWorld
  },
  data() {
    return {
      age: 30,
      data: {}
    };
  },
  mounted() {
    
    //let url = "https://www.easy-mock.com/mock/5ecc5f124790a7228838600a/api-devops/restful/1/list";
    // axios.get(url).then(res => {
    //   console.log(res);
    // });

    // let jsonpUrl = 'https://www.imooc.com/common/adver-getadverlistbymarking?marking=global_newcomer';
    // jsonp(jsonpUrl,(err,res)=>{
    //   this.data = res;

    // })

    let proxyUrl = "/common/adver-getadverlistbymarking?marking=global_newcomer";
    axios.get(proxyUrl).then(res => {
      console.log(res);
    })
  }
};
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
