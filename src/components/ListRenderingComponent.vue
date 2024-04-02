<template>
    <h2>List Rendering Component</h2>
   <div v-if="showConditionalContent">
      <p>This is the conditional content.</p>
    </div>
    
    <!-- Iterative Rendering using v-for -->
    <ul>
      <li v-for="item in itemList" :key="item.id">{{ item.name }}</li>
    </ul>

</template>

<script>
 
export default {
  name: 'ListRenderingComponent',
  data() {
    return {
      showConditionalContent: true,
       showHelloWorld: false,
      itemList: [
        { id: 1, name: 'Item 1' },
        { id: 2, name: 'Item 2' },
        { id: 3, name: 'Item 3' },
      ]
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
