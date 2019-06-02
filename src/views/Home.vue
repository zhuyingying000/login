<template>
  <el-container>
    <el-aside width="240px">
      <LeftNav/>
    </el-aside>
    <el-main>
      <router-view/>
    </el-main>
  </el-container>
</template>

<script>
  import LeftNav from '../components/LeftNav.vue'

  export default {
    name: 'home',
    data () {
      return {
        radio: '1'
      }
    },
    components: { LeftNav }

  }
</script>


