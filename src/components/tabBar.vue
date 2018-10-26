<template>
    <ul class="tabBar">
     <li>
       <a href="">首页</a>
     </li>
      <li>
        <a href="">福利社</a>
      </li>
      <li>
        <a href="">购物车</a>
      </li>
      <li>
        <a href="">我的</a>
      </li>
    </ul>
</template>

<script>
    export default {
        name: "tabBar"
    }
</script>

<style scoped lang="less" rel="stylesheet/lesss">
  @red:#ff0000;
.tabBar{
 display: flex;
  flex-direction: row;
  justify-content: space-around;
}
</style>
