<template>
    <h2>List Rendering Component</h2>
   <!-- Click Event -->
  <div id="clickExample">
    <button @click="toggleValue">Toggle Value</button>
    <p>Boolean Value: {{ booleanValue }}</p>
  </div>
  <div id="inputExample">
    <input v-model="inputText">
    <p>{{ inputText }}</p>
  </div>
    <!-- Mouseover Event -->
    <div id="mouseoverExample">
      <div @mouseover="changeTextColor">Hover over me!</div>
    </div>

    <!-- Submit Event -->
  <div id="submitExample">
    <form @submit.prevent="submitForm">
      <input v-model="formInput" placeholder="Enter value" required>
      <button type="submit">Submit</button>
    </form>
  </div>
<!-- Keydown Event -->
<div id="keydownExample">
  <input @keydown="handleKeyDown" placeholder="Press a key">
</div>
</template>

<script>
    export default {
      name: 'TestEvents',
      data() {
        return {
            booleanValue: false,
            inputText: ''
        };
      },
      methods: {
        toggleValue() {
          this.booleanValue = !this.booleanValue;
        },
        submitForm() {
          alert('Form submitted with value: ' + this.formInput);
        },
        handleKeyDown() {
          alert('Key pressed inside input field!');
        }
      }
    }
    </script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
