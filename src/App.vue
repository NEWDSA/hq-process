<template>
  <div id="app">
    <!--操作结果提示-->
    <msg v-if="errorShow">
      <template slot="description">
        <p class="title">登录失败!</p>
        <p>请求登录时发生错误,请重新尝试!</p>
      </template>
    </msg>
    <template v-else>
      <my-header></my-header>
      <router-view />
    </template>
  </div>
</template>
<script>
import Header from '@/components/Header'
import Msg from '@/views/Msg'
export default {
  name: 'app',
  components: {
    'my-header': Header /* 头部导航 */,
    // 'my-bottom-normal':BottomNormal /* */
    Msg
  },
  data () {
    return {
      transitionName: 'slide-right',
      initPromise: '',
      errorShow: true
    }
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  .title{
    color:#333;
    font-size: 1rem;
    margin-bottom: .25rem;
    p{
      font-size: .8rem;
    }
  }
}
</style>
