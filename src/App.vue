<template>
  <div id="app">
    <h1>
      Poem 10
    </h1>
    <br/>
    <div>
      <p>The right syllable count</p>
      <VueNumberInput v-model="exactSyllableCount" :min="1" :max="100" inline center controls></VueNumberInput>
    </div>
     <br/>
    <LinedTextarea
      :exactSyllableCount="exactSyllableCount"
      :disabled="disable"
      :nowrap="nowrap === 'true'"
      :validate="validate"
      :styles="{ height: height + 'px', width: width + 'px', resize }"
      v-model="content"
    ></LinedTextarea>
  </div>
</template>

<script>
// import Poem from './components/Poem.vue'
import LinedTextarea from "./components/LinedTextarea.vue";
import VueNumberInput from "@chenfengyuan/vue-number-input";
import "./reset.css";
export default {
  name: "App",
  components: {
    LinedTextarea,
    VueNumberInput
  },
  data() {
    return {
      exactSyllableCount: 10
    };
  }
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
</style>
