<template>
  <div>
      <my-header></my-header>
      <h1>页面主体</h1>
  </div>
</template>
<script>
import myHeader from '../components/myHeader.vue';
export default {
    head:{
        title:'简书-创作你的创作',
        meta:[
            {charset:'utf-8'},
            {name:'keywords',content:'简书首页'},
            {name:'description',content:'简书首页'},
            {name:'Author',content:'chen'}
        ]
    },
  data() {
    return {
      name: "首页"
    };
  },
  components:{
      myHeader
  }
};
</script>
<style>

</style>

