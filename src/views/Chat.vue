<template>
  <div class="chat-container">
    <h2>聊天页面</h2>
    <div class="chat-box">
      <!-- 这里可以添加聊天内容 -->
    </div>
    <div class="input-area">
      <el-input v-model="message" placeholder="请输入消息"></el-input>
      <el-button type="primary" @click="sendMessage">发送</el-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: ''
    }
  },
  methods: {
    sendMessage() {
      // 发送消息的逻辑
      console.log('发送消息:', this.message)
      this.message = ''
    }
  }
}
</script>

<style scoped>
.chat-container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.chat-box {
  width: 400px;
  height: 300px;
  border: 1px solid #ccc;
  margin-bottom: 20px;
  overflow-y: auto;
}

.input-area {
  display: flex;
  width: 400px;
}

.input-area .el-input {
  flex: 1;
  margin-right: 10px;
}
</style>