<template>
<div>
  <!-- <li v-for="(item, index) in list" :key="index"> -->
    <h1>TOTAL</h1>
    <treeitem :list="list"></treeitem>
  <!-- </li> -->
</div>
</template>

<script>
import treeitem from './treeitem.vue'
export default {
  components:{
    treeitem
  },
  data() {
    return {
      list: [{
            name: "菜单1",
            cList: [{
                name: "菜单1-1"
              },
              {
                name: "菜单1-2",
      
                cList: [{
                  name: "菜单1-2-1",
        
                  cList: [{
                    name: "菜单1-2-1-1"
                  }]
                }]
              }
            ]
          },
          {
            name: "菜单2"
          },
          {
            name: "菜单3",
            cList: [{
              name: "菜单3-1"
            }, {
              name: "菜单3-2",
              cList:[{
                name:'菜单3-2-1'
              }]
            }]
          }
        ]
    };
  },
  mounted() {},
  methods: {
  }
};
</script>

<style lang="less" scoped>

</style>