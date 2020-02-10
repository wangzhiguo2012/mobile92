<template>
  <div class="container">
    <!-- 导航栏
      title:导航栏 中间信息
      right-text 右侧信息
      fixed：导航栏 固定在头部
      @click-right： 右侧文字单击事件
     -->
    <van-nav-bar fixed title="黑马头条" right-text="搜索"
      @click-right="$router.push('/search')"/>

    <div class="my-wrapper" >
      <router-view></router-view>
    </div>

    <!-- 标签栏，特点，页面底部显示
      van-tabbar
          route:开启路由
          v-model：设置指定标签激活，如果使用route路由模式，就不用设置这个属性了
      van-tabbar-item
          to：设置路由跳转地址的
          icon：标签显示图表的
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
