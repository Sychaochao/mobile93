<template>

  <div class="container">
    <!-- 公共头部
    van-nav-bar是 导航栏组件，
    title：导航中间呈现内容
    -->
    <van-nav-bar fixed title="超超头条" right-text="搜索"
      @click-right="$router.push('/search')"/>

    <div class="my-wrapper" >
      <!--路由占位符，用于显示 home、question、video、user的组件的-->
      <router-view></router-view>
    </div>

    <!-- 公共脚步
      van-tabbar:标签栏组件
      van-tabbar: route  激活路由功能
      van-tabbar-item
        to: 请求路由地址
        icon：标签栏项目显示的图标，icon图标库在组件库中可以看到
    -->
    <van-tabbar route>
      <van-tabbar-item to="/home" icon="home-o">首页</van-tabbar-item>
      <van-tabbar-item to="/question"  icon="chat-o">问答</van-tabbar-item>
      <van-tabbar-item to="/video"  icon="video-o">视频</van-tabbar-item>
      <van-tabbar-item to="/user"  icon="user-o">我的</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped lang='less'>
.container{
  width: 100%;
  height: 100%;
  position: relative;
  .my-wrapper{
    width: 100%;
    height: 100%;
    overflow: hidden;
    padding-top: 92px;
    padding-bottom: 100px;
    box-sizing: border-box;
    &.noTop{
      padding-top: 0;
    }
  }
}
</style>
