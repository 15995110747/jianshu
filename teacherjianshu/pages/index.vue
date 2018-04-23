<template>
    <div style="height:100%">
       <my-header></my-header>
    </div>
</template>
<script>
    import myHeader from  '../components/myHeader'
    export default {
        head:{
            title:'简书-创作你的创作',
            meta:[
                {charset:'utf-8'},
                {name:'keywords',content:'简书首页'},
                {name:'description',content:'简书首页'},
                {name:'author',content:'李志远'}
            ]
        },
        components:{
            myHeader
        },
        data () {
            return {
                name:'首页'
            }
        }
    }
</script>
<style>

</style>