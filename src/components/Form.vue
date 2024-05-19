<template>
    <div class="form">
      <form @submit.prevent="addItem">
        <input v-model="newItem" placeholder="Add new value">
        <button class="custom-button" type="submit">Add</button>
      </form>

      <ul>
        <li v-for="(item, index) in items" :key="index">
          {{ item }}
          <button class="custom-button" @click="removeItem(index)">Delete</button>
        </li>
    </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newItem: '',
        items: []
      };
    },
    methods: {
      addItem() {
        if (this.newItem !== '') {
          this.items.push(this.newItem);
          this.newItem = '';
        } else {
            alert('Please enter a valid value');
        }
      },
      removeItem(index) {
        this.items.splice(index, 1);
      }
    }
  };
  </script>
  
  <style scoped>
  form {
    margin-bottom: 20px;
  }
  input {
    margin-right: 10px;
  }
  button {
    margin-left: 10px;
  }
  </style>
  