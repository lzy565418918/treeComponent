<template>
<div>
  <ul v-for="(item, index) in list.cList" :key="index">
    <treeitem :list="list"></treeitem>
  </ul>
</div>
</template>

<script>
import treeitem from './treeitem.vue'
export default {
  props: ["list"],
  components:{
    treeitem
  },
  data() {
    return {
      show: false
    };
  },
  mounted() {},
  methods: {
  }
};
</script>

<style lang="less" scoped>
div {
  text-align: left;
  padding-left: 20px !important;
}
</style>