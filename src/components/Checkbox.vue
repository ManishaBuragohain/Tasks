<template>
<h1>Task 3</h1>
    <div>
        <input type="text" placeholder="enter a text" v-model="name"> <br><br>
        <button @click="getResult">Get Result</button>

        

    </div>
</template>

<script>
    export default {
        data(){
            return{
                name : "",
            };
        },
        methods:{
            getResult(){
                alert(this.name);
            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>