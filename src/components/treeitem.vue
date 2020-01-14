<template>
  <li>
    <span>{{list.name}}</span>
    <ul v-show="show">
      <treeitem v-for="(item, index) in list.cList" :key="index"></treeitem>
    </ul>
  </li>
</template>

<script>
export default {
  props: ["list"],
  name: "treeitem",
  data() {
    return {
      show: false
    };
  },
  mounted() {},
  methods: {
    changeStatus() {
      this.show = !this.show;
    }
  }
};
</script>

<style lang="less" scoped>
</style>