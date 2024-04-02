<template>
  <div class="hello">
   <ChildComp foodName="Food Name!"/>
  </div>
</template>

<script>
export default {
  name: 'ParentComp',
   data() {
        return {
            booleanValue: false,
            inputText: '',
            longList: Array.from({ length: 100 }, (_, index) => `Item ${index + 1}`)
        };
      }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>