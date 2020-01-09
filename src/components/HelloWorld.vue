<template>
  <div>
    <tree :list="list"></tree>
  </div>
</template>

<script>
  import tree from "@/components/tree";
  export default {
    components: {
      tree
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
              name: "菜单3-2"
            }]
          }
        ]
      };
    }
  };
</script>

<style>
</style>