<template>
  <el-menu default-active="2" class="el-menu-vertical-demo menu-user">
    <el-sub-menu index="1">
      <template #title>
        <el-icon><House /></el-icon>
        <span>首页</span>
      </template>
      <el-menu-item-group title="Group One">
        <el-menu-item index="1-1">item one</el-menu-item>
        <el-menu-item index="1-2">item two</el-menu-item>
      </el-menu-item-group>
      <el-menu-item-group title="Group Two">
        <el-menu-item index="1-3">item three</el-menu-item>
      </el-menu-item-group>
      <el-sub-menu index="1-4">
        <template #title>item four</template>
        <el-menu-item index="1-4-1">item one</el-menu-item>
      </el-sub-menu>
    </el-sub-menu>
    <el-menu-item index="2">
      <el-icon><RefreshLeft /></el-icon>
      <span>最近</span>
    </el-menu-item>
    <el-menu-item index="3">
      <el-icon><Share /></el-icon>
      <span>分享</span>
    </el-menu-item>
    <el-menu-item index="4">
      <el-icon><Lock /></el-icon>
      <span>隐藏空间</span>
    </el-menu-item>
    <el-menu-item index="5">
      <el-icon><UserFilled /></el-icon>
      <span>我的</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {

}
</script>

<style>
.menu-user{
  border: 0;
}
</style>