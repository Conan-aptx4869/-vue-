<template>
    <div class="header">
        <div id="logo">{{logo}}</div>
      <ul class="nav">
        <li v-for="nav in navs">{{nav.li}}</li>
      </ul>
      <div>
        <h1>子组件部分</h1>
        <!--<p>{{message}}</p>-->
        <button @click="sendMsgToParent">向父组件传值</button>
      </div>
    </div>
</template>

<script>
    export default {
      name:'Child',
      data () {
        return {
          username:'',
          navs:[
            {li:'home'},
            {li:'abouts'},
            {li:'contact'},
            {li:'map'}
            ]
        }
      },
      props:['logo'],
      methods:{
        sendMsgToParent () {
          this.$emit("parentData","this is message is from child")
        }
      }
    }
</script>

<style scoped>

</style>
