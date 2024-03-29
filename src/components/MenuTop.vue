<template>
    <el-menu
    :default-active=route_name
    class="el-menu-demo"
    mode="horizontal"
    :ellipsis="false"
  >
    <el-menu-item style="font-size: larger; color: cornflowerblue;" >
      Dawn云盘
    </el-menu-item>
    <div class="flex-grow" />
    <router-link to="login" style="text-decoration: none;">
      <el-menu-item index="login">
        登录
      </el-menu-item>
    </router-link>
    <router-link to="register" style="text-decoration: none;">
      <el-menu-item index="register">
        注册
      </el-menu-item>
    </router-link>
  </el-menu>
</template>

<script>
import {useRoute} from "vue-router";
import { computed } from 'vue';
export default {
  setup(){
        const route = useRoute();
        let route_name = computed(() => route.name);
        console.log(route_name)
        return {
            route_name
        }
    },
}
</script>

<style>

</style>