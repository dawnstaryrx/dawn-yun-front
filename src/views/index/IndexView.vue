<template>
  <el-container style="height: 100%; padding:0;">
    <el-aside width="200px" style="background-color: aliceblue;height: 100%;">
      <h5 class="mb-2" style="text-align: center; font-size: larger;">Dawn网盘</h5>
      <menu-user-vue></menu-user-vue>
    </el-aside>
    <el-container>
      <el-header>Header</el-header>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
import MenuUserVue from '@/components/MenuUser.vue'
export default {
  components:{MenuUserVue}
}
</script>