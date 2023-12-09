<script>
  export default {
    data() {
      return {
        message: '',
        clickResult : ''
      }
    },
    methods: {
      upperMessage () {
        return this.message.toUpperCase() + "!!!";
      },

      handleClick(){
        this.clickResult = this.message + 1;
      } 
    }
  }
</script>

<template>
  <main>
      <container class="container">
        <h4>the current count is...</h4>
        <p>Message is: {{ upperMessage() }}</p>
        <input v-model="message" placeholder="edit me" />
        <button @click="handleClick()">Click me</button>
        <h5>You have clicked : {{ clickResult }}</h5>
      </container>
  </main>
</template>
