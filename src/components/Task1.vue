<template>
  <div>
    <h1>Task 1</h1>
    <button v-on:click="Even">even numbers- {{ EvenNumbers }}</button> <br /><br />
    <button v-on:click="Odd">odd numbers -{{ oddNumbers}}</button>
     </div>

     
<div>
  

</div>
</template>

<script>
export default {
  data() {
    return {
      num: [1, 2, 3, 4, 5],
      oddNumbers : null,
      EvenNumbers : null,

    };
  },
  methods: {
    Odd() {
      let oddresult = this.num.filter((val) => {
        if (val % 2 != 0) return val;
      });
       console.log(oddresult);
       this.oddNumbers = oddresult;
      alert("Odd Numbers " + oddresult);
    },

    Even() {
      let Evenresult = this.num.filter((val) => {
        if (val % 2 == 0) return val;
      });
      console.log(Evenresult);
      this.EvenNumbers = Evenresult;
      alert("Even Numbers " + Evenresult);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>