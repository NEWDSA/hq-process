<template>
  <div class="container">
    <div class="menu"><van-icon name="chat-o"  size="40" /></div>
    <!--具名插槽-->
    <slot name="description" class="menu"></slot>
  </div>
</template>
<style lang="scss" scoped>
.container {
  width: 100%;
  height: 200px;
  background: gray;
  .menu {
      position: relative;
      top: 10px;
  }
}
</style>
