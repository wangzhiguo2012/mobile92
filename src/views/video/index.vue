<template>
  <div class='container'>
    <!-- 骨架屏
    内容占位标签，待内容准备好了，骨架屏消失，显示业务内容
    title: 第一行内容
    row：设置行数显示
    avatar：小圆圈
     -->
    <van-skeleton title avatar :row="3" />
    <van-skeleton title avatar :row="3" />
    <van-skeleton title avatar :row="3" />
  </div>
</template>

<script>
export default {
  name: 'video-index'
}
</script>

<style scoped lang='less'>
.van-skeleton{
  margin-top: 10px;
}
</style>
