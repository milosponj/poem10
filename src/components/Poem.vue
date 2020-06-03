<template>
  <div>
    <p>this is a poem</p>
    <textarea rows = "50" cols = "60" v-model="poem">
    </textarea>
    <p>{{text}}</p>
    <p>{{next}}</p>
  </div>
</template>

<script>
var syllable = require('syllable')
export default {
  name: 'HelloWorld',
  data: ()=>({
    poem:"",
    text: "hello!",
    next: syllable(this.poem)
  })
}
</script>


<style>
.poem-input {
  height: 100px;
  width: 100px;
}
</style>