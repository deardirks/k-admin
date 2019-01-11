<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>Home page</h1>
    <button @click="getUser()">获取用户信息</button>
  </div>
</template>

<script>
import axios from "axios";
import "@/mock/mock.js";
export default {
  name: "home",
  methods: {
    getUser() {
      axios.get("http://localhost:8080/user").then(res => {
        alert(JSON.stringify(res.data));
      });
    }
  }
};
</script>
