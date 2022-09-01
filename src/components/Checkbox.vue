<template>
  <h2>Task 4</h2>
          <form>
            <div class="form-group">
              <label for="todoitem">Add Datas :</label><br />
              <input
                type="text"
                v-model="input"
                class="form-control"
                id="todoitem"
                placeholder="add"
              />
            </div>
            <br /><br />
            <button type="button" v-on:click="add()" class="storebtn">
              Store
            </button>
          </form>
       
   
        <h2>Results</h2>
        <div class="list-group">
          <p
            v-for="(todo, index) in todos"
            :key="index"
            class="list-group-item"
          >
            {{ todo }}
          </p>
        </div>
    

</template>

<script>
export default {
  name: "Todo",
  data() {
    return {
      todos: [],
      input: "",
    };
  },
  methods: {
    add() {
    //   this.todos.push(this.input);
    //   this.input = "";
        this.todos.push(this.input);
       this.todos = [ ...new Set(this.todos) ]
    },
  },
};
</script>

<style>
.storebtn {
  width: 80px;
}

input[type="text"],
select {
  width: 20%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>