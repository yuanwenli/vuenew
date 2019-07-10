<template>
   <div>
      <button @click="onClick" >anniu</button>
      <transition name="fade">
         <div :is="Comment"></div>
         <!--<h1 v-show="show">enter</h1>-->
      </transition>

   </div>

</template>

<script>
   import  Acom from "../../components/a"
   import  Bcom from "../../components/b"

   export default {
      components: {
      Acom,
      Bcom
   },
        name: "index",
       data(){
           return{
              show:true,
              Comment:"Acom"
           }
       },
       created(){
           console.log(this.show)
       },
       methods:{
          onClick(){
             if(this.Comment==="Acom"){
                this.Comment="Bcom"
             }else{
                this.Comment="Acom"
             }
          }
       }
    }
</script>

<style scoped>
   /*.fade-enter-active, .fade-leave-active {*/
      /*transition: opacity 2s;*/
   /*}*/
   /*.fade-enter, .fade-leave-to  {*/
      /*opacity: 0;*/
   /*}*/
</style>