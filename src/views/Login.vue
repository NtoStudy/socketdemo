<template>
  <el-container class="login-container">
    <el-main>
      <el-row justify="end">
        <el-col :span="10">
          <el-card class="login-card">
            <h2 class="login-title">用户登录</h2>
            <el-form :model="form" label-width="80px">
              <el-form-item label="用户名">
                <el-input v-model="form.username" placeholder="请输入用户名" />
              </el-form-item>
              <el-form-item label="密码">
                <el-input v-model="form.password" type="password" placeholder="请输入密码" />
              </el-form-item>
              <el-form-item>
                <el-button type="primary" @click="handleLogin">登录</el-button>
                <el-button>注册</el-button>
              </el-form-item>
            </el-form>
          </el-card>
        </el-col>
      </el-row>
    </el-main>
  </el-container>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  username: '',
  password: ''
})

const handleLogin = () => {
  // 处理登录逻辑
}
</script>

<style lang="scss" scoped>
.login-container {
  height: 100vh;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);

  .login-card {
    margin-right: 150px;
    margin-top: 150px;
    padding: 20px;
    border-radius: 8px;

    box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);

    .login-title {
      text-align: center;
      margin-bottom: 20px;
      color: #303133;
    }

    .el-form-item {
      margin-bottom: 20px;
    }

    .el-button {
      width: 100%;
      margin-top: 10px;
    }
  }
}
</style>
