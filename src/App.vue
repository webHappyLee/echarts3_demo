<template>
  <div id="app">
    <el-container>
      <el-aside class="aside"><Aside></Aside></el-aside>
      <el-container>
        <el-header>echarts图例展示</el-header>
        <el-main>
          <router-view />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import Aside from "@/components/Aside";
export default {
  components: { Aside },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.aside {
  height: 100vh;
}
</style>
