<template>
  <menu-top></menu-top>
  <el-row type="flex" justify="center" align="middle" :gutter="20" style="padding-top: 5%;">
      <el-card style="max-width: 600px; text-align: center; align-items: center;">
        <h3>登录</h3>
        <el-form
          style="max-width: 600px"
          status-icon
          label-width="auto"
          class="demo-ruleForm"
          :rules="basicRoles"
          :model="loginInfo"
        >
          <el-form-item label="用户名" prop="username">
            <el-input v-model="loginInfo.username" type="text" autocomplete="off" />
          </el-form-item>
          <el-form-item label="密码" prop="pwd">
            <el-input v-model="loginInfo.pwd" type="password" autocomplete="off" />
          </el-form-item>
          <el-form-item>
            <el-button type="primary">提交</el-button>
            <el-button @click="reset()">重置</el-button>
            <div style="padding-left: 20px;">没有账号，去
              <router-link to="register" style="text-decoration: none;">注册</router-link>
            </div>
          </el-form-item>
        </el-form>
      </el-card>
  </el-row>
</template>

<script>
import { useRoute } from "vue-router";
import { computed } from 'vue';
import MenuTop from '@/components/MenuTop.vue';

export default {
  components:{MenuTop},
  setup(){
        const route = useRoute();
        let route_name = computed(() => route.name);
        console.log(route_name)
        return {
            route_name
        }
    },
  data(){
    return{
      loginInfo:{
        username:"",
        pwd:"",
      },
      basicRoles:{
        username:[{ required: true, message: '请输入用户名', trigger: 'blur' }],
        pwd:[{ required: true, validator: this.validatePwd, trigger:'blur' }],
      },
    }
  },
  methods:{
    validatePwd(rule, value, callback){
      if(!value || value.length == 0){
        callback(new Error('请输入密码！'))
      }else{
        callback()
      }
    },
    reset(){
      this.loginInfo.username = "";
      this.loginInfo.pwd = "";
    }
  }
}
</script>



<style>
.flex-grow {
  flex-grow: 1;
}
</style>