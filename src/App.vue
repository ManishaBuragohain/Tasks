<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
<title>Calculator</title>
<div class="container">
  <div class="row">
     <div class="col-md-12"><h1 align = "center">Calculator Task</h1></div>
     <div class="col-md-1">
            <label class="label">First Number </label> <br>
            <input type="number" name="firstnum" class="form-control" v-model="firstNum" />
          </div>
          <br><br>
           <div class="col-md-3">
            <label class="label">Second Number</label> <br>
            <input type="number" name="secndNum" class="form-control" v-model="secndNum"/>
          </div>


  </div>
  <br><br>
    <div class="row">
            <div class="col-md-1" style="display:inline">
              <Add :num1="firstNum" :num2="secndNum" @result="getResult"></Add></div>
              <Mult :num1="firstNum" :num2="secndNum" @result="getResult"></Mult>
             <Sub :num1="firstNum" :num2="secndNum" @result="getResult"></Sub>
              <Divide :num1="firstNum" :num2="secndNum" @result="getResult"></Divide>
          </div>
           <p> OUTPUT </p>
          <button class="result"> <span> {{result}}</span> </button>
      </div>





  <Task1 />
  <Task2 />
  <Task3 /> <br>

  <Checkbox/>
 
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Add from "./components/Add.vue";
import Sub from "./components/Sub.vue";
import Divide from "./components/Divide.vue"
import Mult from "./components/Mult.vue"
import Task1 from "./components/Task1.vue";
import Task2 from "./components/Task2.vue";
import Task3 from "./components/Task3.vue";
import Checkbox from "./components/Checkbox.vue";

export default {
  name: "App",
 data(){
   return{
        firstNum:"",
      secndNum:"",
      result:""

   }
 },
 methods:{
   getResult(val){
     this.result=val
   }

 }
,
  components: {
    Task1,
    Task2,
    Task3,
    Add,
    Mult,
    Sub,
    Divide,
    Checkbox
    
   
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.row{
  display: inline;
}
.btnclss{
     background-color: rgb(192, 166, 156);
  border: none;
  color: black;
  padding: 15px 32px;
  text-align: center;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  display: inline-block;
}
input[type=number], select {
  width: 20%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
.label{
  color: red;
  font-size: 20px;
}
.result{
   background-color: rgb(164, 164, 184);
  border: #2c3e50;
  color: black;
}



</style>
