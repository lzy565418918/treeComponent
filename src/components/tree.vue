<template>
  <div>
      <div v-for="(item, index) in list" :key="index">
        <span @click="changeStatus(index)">{{item.name}}</span>
        <tree v-if="show" :list="item.cList"></tree>
      </div>
  </div>
</template>

<script>
export default {
  props: ["list"],
  name: "tree",
  data() {
    return {
        show:false
    };
  },
  methods: {
      changeStatus(idx){
          this.show = !this.show
      }
  },
};
</script>

<style lang="less" scoped>
div {
    text-align: left;
    padding-left: 20px !important;
}
</style>