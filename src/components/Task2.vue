<template>
  <h1>Task 2</h1>
  <div class="hello">
    <button
      class="btn"
      @click="activeButton = 0"
      v-bind:style="{ 'background-color': buttonColor[0] }"
    >
      1</button
    ><br />
    <button
      class="btn"
      @click="activeButton = 1"
      v-bind:style="{ 'background-color': buttonColor[1] }"
    >
      2</button
    ><br />
    <button
      class="btn"
      @click="activeButton = 2"
      v-bind:style="{ 'background-color': buttonColor[2] }"
    >
      3</button
    ><br />
    <button
      class="btn"
      @click="activeButton = 3"
      v-bind:style="{ 'background-color': buttonColor[3] }"
    >
      4</button
    ><br />
    <button
      class="btn"
      @click="activeButton = 4"
      v-bind:style="{ 'background-color': buttonColor[4] }"
    >
      5</button
    ><br />
  </div>
</template>

<script>
export default {
  name: "Task2",
  data() {
    return {
      activeButton: 0,
    };
  },
  computed: {
    buttonColor: function () {
      let result = [];
      for (var i = 0; i <= 5; i++) {
        if (this.activeButton == i) {
          result.push("red");
        } else {
          result.push("white");
        }
      }

      return result;
    },
  },
};
</script>
<style>
button {
  border: black;
  border-color: black;
  border-style: solid;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>