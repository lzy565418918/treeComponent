<template>
  <div>
    <li v-for="(item, index) in list" :key="index">
      <span @click.stop="changeStatus">{{item.name}}</span>
      <treeitem v-show="show" :list='item.cList'></treeitem>
    </li>
  </div>
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
div {
  text-align: left;
  padding-left: 20px !important;
}
</style>