<template>
  <div id="app">
      <el-menu
        :router="true"
        class="el-menu-demo"
        mode="horizontal"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="/">Comptes</el-menu-item>
      </el-menu>
      <h1>Administration comptable</h1>
  </div>
</template>

<style scoped lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: black;

    nav {
      padding: 30px;
    }

    nav a {
      font-weight: bold;
      color: #2c3e50;
    }
  }
</style>
