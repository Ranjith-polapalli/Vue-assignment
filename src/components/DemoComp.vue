<template>
  <div class="hello">
    <h1>Hi {{ userName }} Product - {{ productName }} productPrice - {{ productPrice }} LastUpdatedDate - {{ formattedDate  }}</h1>
    <p v-html='content'></p>
    <p v-text="pText"></p>
    <h1>Using computed the sum is - {{ sum }}</h1>
    <div :class="{ 'red': isRed }">
      <!-- Content of the div -->
      Styling changes based on isRed value
    </div>

    <button :title="buttonTitle" @click="changeTitle"> Click me </button>
  </div>
</template>

<script>
export default {
  name: 'DemoComp',
  data() {
    return {
      userName: 'Ranjith',
      productName: 'Test Product',
      lastUpdated: new Date(),
      productPrice: 50,
      content:"<p> Html Content using v-html</p>",
     pText: 'This is the new text!',
     buttonTitle: 'Initial Title',
     isRed:true,
     number1:4,
     number2:6
    };
  },
  computed: {
    formattedDate() {
      // Format the date using your preferred method
      console.log("formattedDate "+this.lastUpdated)
      console.log("formattedDate  toLocaleDateString "+this.lastUpdated.toLocaleDateString)
      return this.lastUpdated.toLocaleDateString();
    },
    sum() {
      return this.number1 + this.number2;
    }
  },
  methods: {
    changeTitle() {
      // Change the value of buttonTitle dynamically
      this.buttonTitle = "New Title",
      this.isRed = !this.isRed
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
.red {
  color: red;
  /* Add any other styles you want to apply when isRed is true */
}
</style>
