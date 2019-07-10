<template>
    <HelloWorld @commonEvent="getEvent" :myvalue="value" :data="list">
        <p slot="header">xxx--header</p>
        <p slot="footer">xxx--footer</p>
    </HelloWorld>
</template>

<script>
    import Vue from "vue"
    import HelloWorld from "../../components/HelloWorld"
    export default {
        name: "home",
        components:{
            HelloWorld,
        },
        data(){
           return{
               value:"我的学生",
               list:[
                   {
                   name:"zhangsan",
                   age:55
                   },
                   {
                       name:"lisi",
                       age:22
                   }
               ]
           }
        },
        methods:{
            getEvent(msg){
                console.log(msg)
            }
        }
    }
</script>

<style scoped>

</style>