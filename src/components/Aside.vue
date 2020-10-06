<!-- 导航菜单 -->
<template>
  <div>
    <el-menu
      :default-openeds="['5']"
      v-for="(item, index) in navList"
      :key="index"
    >
      <el-submenu :index="`${index + 1}`">
        <template slot="title"
          ><i class="el-icon-message"></i>{{ item.name }}</template
        >
        <template v-if="item.children.length">
          <el-menu-item
            :index="`${index + 1}-${ind + 1}`"
            v-for="(it, ind) in item.children"
            :key="ind"
            @click="goToPath(it.path)"
            >{{ it.name }}</el-menu-item
          >
        </template>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {
      navList: [
        { name: "折线图", children: [] },
        { name: "柱状图", children: [] },
        { name: "饼图", children: [] },
        { name: "散点图", children: [] },
        {
          name: "地理坐标/地图",
          children: [
            { name: "世界地图", path: "/map" },
            { name: "中国地图", path: "/china" },
            { name: "GEO中国地图", path: "/geoIndex" },
            { name: "地图迁徙", path: "/moveMap" },
          ],
        },
        { name: "K线图", children: [] },
        { name: "雷达图", children: [] },
        { name: "盒须图", children: [] },
        { name: "热力图", children: [] },
        { name: "关系图", children: [] },
        { name: "路径图", children: [] },
        { name: "树图", children: [] },
        { name: "矩形树图", children: [] },
        { name: "旭日图", children: [] },
        { name: "平行坐标图", children: [] },
        { name: "漏斗图", children: [] },
      ],
    };
  },

  computed: {},

  created() {},

  mounted() {},

  methods: {
    goToPath(path) {
      this.$router.push(path);
    },
  },
};
</script>
<style lang='less' scoped>
</style>