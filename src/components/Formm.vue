<template>
    <div>
      <form @submit.prevent="submitForm">
        <label>
          Name:
          <input type="text" v-model="name" required>
        </label>
        <label>
          Email:
          <input type="email" v-model="email" required>
        </label>
        <label>
          Message:
          <textarea v-model="message" required></textarea>
        </label>
        <button type="submit">Submit</button>
      </form>
    </div>
  </template>
  <script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: ''
      }
    },
    methods: {
      submitForm() {
        axios.post('http://localhost:3000', {
          name: this.name,
          email: this.email,
          message: this.message
        })
          .then(response => {
            // handle success response here
          })
          .catch(error => {
            // handle error response here
          });
      }
    }
  };
  </script>