<template>
  <div>
    <tree :data="tree" :node-text="name" layoutType="circular" class="tree">
    </tree>
  </div>
</template>

<script>
import {tree} from 'vued3tree'

export default {
  components: {
    tree
  },
  data() {
    return {
      tree: {
        name: "father",
        children:[{
          name: "son1",
          children:[ {name: "grandson"}, {name: "grandson2"}]
        },{
          name: "son2",
          children:[ {name: "grandson3"}, {name: "grandson4"}]
        }]
      }
    }
  }
}
</script>

<style>
.tree {
  width: 100%;
  height: 100%;
}
</style>
