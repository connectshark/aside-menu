<template>
  <header>
    <div class="menu-icon" @click="asideHandler(true)">
      <img src="../assets/icon/menu.png" alt="menu">
    </div>
    <h1>我這裡是header</h1>
  </header>
</template>

<script>
export default {
  props: ['asideHandler']
}
</script>

<style lang="scss" scoped>
header{
  padding: 20px 10px;
  box-sizing: border-box;
  background-color: #fbc2eb;
  position: relative;
  h1{
    font-size: 20px;
  }
  .menu-icon{
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    left: 10px;
    width: 40px;
    height: 40px;
    img{
      vertical-align: middle;
      width: 100%;
    }
  }
}
</style>