<template>
    <div>
  <input type="button" value="addition" @click="addNum" class="btnclss" >
    </div>
</template>

<script>
    export default {
        name : "Add",
        data(){
           return {
               addResult:"",
           }


           },
           props:['num1','num2'],
           methods:{
               addNum(){
                 this.addResult = 0;
                 this.addResult= this.num1+this.num2;
                 this.$emit("result",this.addResult)

               }

           }
           
        }
        
    
</script>

<style>

</style>