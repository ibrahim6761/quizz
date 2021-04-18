<template>
  <div id="app">
    <h1>Matematik Sınav Uygulaması</h1>
    <OperatorQuiz @onBack="onBack" v-if="operator" :operator="operator"></OperatorQuiz>
    <OperatorSelector v-if="!operator" @changeOperator="changeOperator"></OperatorSelector></div>
</template>

<script>
import OperatorSelector from "@/components/OperatorSelector";
import OperatorQuiz from "@/components/OperatorQuiz";
export default {
  name: 'App',
  data (){
    return {
      operator : null,
    }
  },
  methods: {
    changeOperator(operator) {
      this.operator = operator
    },
    onBack(){
      this.operator = null
    }
  },
  components: {
    OperatorSelector : OperatorSelector,
    OperatorQuiz : OperatorQuiz
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 24px;
}

button{
  padding: 20px;
  width: 200px;
  height: 80px;
  margin-right: 10px;
  background-color: #10aeb2;
  color: white;
  font-size: 24px;
  cursor: pointer;
}
</style>
