<template>
  <div class="aside-bar" @click="asideHandler(false)">
    <div class="aside-content" @click.stop>
      <h2>側邊欄看到囉</h2>
    </div>
  </div>
</template>

<script>
export default {
  props: ['asideHandler']
}
</script>

<style lang="scss" scoped>
.aside-bar{
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, .5);
  z-index: 50;
  .aside-content{
    position: absolute;
    left: 0;
    top: 0;
    width: 30%;
    min-width: 300px;
    height: 100%;
    background-color: #fff;
    h2{
      font-size: 29px;
      line-height: 1.9;
    }
  }
}
</style>