<template>
  <el-col :span="14">
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
    >
      <!-- <el-sub-menu index="1">
        <template #title>
          <span>Navigator One</span>
        </template>
        <el-menu-item-group title="Group One">
          <el-menu-item index="1-1">
          </el-menu-item>
          <el-menu-item index="1-2">item one</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="Group Two">
          <el-menu-item index="1-3">item three</el-menu-item>
        </el-menu-item-group>
        <el-sub-menu index="1-4">
          <template #title>item four</template>
          <el-menu-item index="1-4-1">item one</el-menu-item>
        </el-sub-menu>
      </el-sub-menu> -->

      <el-menu-item index="2">
        <router-link to="/">Home</router-link>
      </el-menu-item>

      <el-menu-item index="3" disabled>
        <!-- <el-icon><document /></el-icon> -->
        <router-link to="/about">About</router-link>
      </el-menu-item>

      <!-- <el-menu-item index="4">
        <el-icon><setting /></el-icon>
        <span>Navigator Four</span>
      </el-menu-item> -->

    </el-menu>
  </el-col>
</template>

<script >

export default {
  name: 'SideBar',
  props: {
    title: String
  },

  data () {
    return {

    }
  },

  methods: {
    handleOpen () {
      console.log('OPEN')
    },
    handleClose () {
      console.log('CLOSE')
    }
  },

  mounted () {
    console.log('TWAS MOUNTED ' + JSON.stringify(this.title))
  }

}
</script>
<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>
