<template>
  <div id="app">
    <child :logo="logoMsg"></child>
    <div>
      <h1>这</h1>
    </div>
    <child :message="parentMsg" @parentData="showMsgFromChild"></child>
    <preview></preview>
  </div>
</template>

<script>
  import child from './components/Child';
  import preview from './components/preview';
  export default {
    data () {
      return {
        logoMsg:'hello,parent',
        parentMsg:'hello,child'

      }
    },
    components: {
      child,
      preview
    },
    methods:{
      showMsgFromChild (data) {
        console.log(data);
      }
    },
    created () {

    }

  }
</script>

<style scoped>

</style>
