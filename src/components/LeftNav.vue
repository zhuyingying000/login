<template>
  <el-menu
      default-active="2"
      @open="handleOpen"
      background-color="#000000"
      text-color="#fff"
      active-text-color="#ffd04b"
      @close="handleClose">
    <el-submenu index="1">
      <template slot="title">
        <i class="el-icon-location"></i>
        <span>导航一</span>
      </template>
      <el-menu-item-group>
        <template slot="title">分组一</template>
        <el-menu-item index="1-1">
          <router-link to="/about" class="while">route-link1</router-link>
        </el-menu-item>
        <el-menu-item index="1-2">
          <router-link to="/Setting" class="while">route-link2</router-link>
        </el-menu-item>
      </el-menu-item-group>
      <el-menu-item-group title="分组二">
        <el-menu-item index="1-3">
          <router-link to="./open" class="while">route-link3</router-link>
        </el-menu-item>
      </el-menu-item-group>
      <el-submenu index="1-4">
        <template slot="title">选项4</template>
        <el-menu-item index="1-4-1">
          <router-link to="./close" class="while">route-link4</router-link>
        </el-menu-item>
      </el-submenu>
    </el-submenu>
    <el-menu-item index="2">
      <i class="el-icon-menu"></i>
      <span slot="title">导航二</span>
    </el-menu-item>
    <el-menu-item index="3" disabled>
      <i class="el-icon-document"></i>
      <span slot="title">导航三</span>
    </el-menu-item>
    <el-menu-item index="4">
      <i class="el-icon-setting"></i>
      <span slot="title">导航四</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
  export default {
    name: 'LeftNav',
    methods: {
      handleOpen (key, keyPath) {
        // console.log(key, keyPath)
      },
      handleClose (key, keyPath) {
        // console.log(key, keyPath)
      }
    }
  }
</script>

<style scoped>

  .menu {
    height: 100% !important;
  }

  .while {
    color: white;
    text-decoration: none;
  }

  .el-menu {
    background-color: #545c64;
    height: 100%;
  }

</style>
