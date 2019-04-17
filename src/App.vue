<template>
  <div id="app">
    <el-container style="border: 1px solid #eee">
      <aside-menu />
      <el-container>
        <el-main>
          <iframe 
            src="http://support.supermap.com.cn:8090/webgl/examples/editor.html#S3MTiles_suofeiya"
            name="s3m三维切片缓存"
            height="100%"
            width="100%"
            scrolling="no"
            seamless/>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script lang="ts">

import AsideMenu from './components/AsideMenu/index.vue';
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component({
  components: {
    AsideMenu
  },
})
export default class App extends Vue {
   
};
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.el-main {
  height: 100vh;
}
</style>
