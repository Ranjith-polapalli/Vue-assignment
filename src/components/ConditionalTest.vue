<template>
  <div class="hello">
   <div v-show="invisible">I am invisible in v-show</div>
   <div v-if="invisible">I am invisible in v-if</div>
   <ul>
      <li v-for="(item, index) in itemList" :key="index">
        {{ index + 1 }}. {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ConditionalTest',
  data() {
    return {
      invisible: false,
      itemList: ["Item 1", "Item 2", "Item 3", "Item 4"],
    }
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