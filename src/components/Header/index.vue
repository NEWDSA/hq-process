<template>
  <van-nav-bar
    title="title"
    left-arrow
    bind:click-left="onClickLeft"
    bind:click-right="onClickRight"
  />
</template>
<script>
export default {
  data () {
    return {
      title: ''
    }
  },
  mounted () {
    // this.title = $route.meta.title
  }
}
</script>
