<template>
  <div class="home">
    <h1>Hi!</h1>
    <Name />
  </div>
</template>

<script>
// @ is an alias to /src
import Name from "@/components/Name.vue";

// const a = 7;
// const stringWithA = `a = ${a}`;

export default {
  name: "home",
  components: {
    Name
  }
  // data: function() {
  //   return {
  //     variableOne: "hi",
  //     variableTwo: ["what, hello?"]
  //   };
  // }
};
</script>

<style lang="scss" scoped>
.home {
  $margin: 50px;

  margin: $margin;
  padding: 50px;
  box-sizing: border-box;
  text-align: center;
  min-height: calc(100vh - #{2 * $margin});

  background: linear-gradient(90deg, #fc466b 0%, #3f5efb 100%);
  color: white;
}
.name {
  text-transform: uppercase;
}
</style>
