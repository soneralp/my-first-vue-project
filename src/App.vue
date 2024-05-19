<script setup>
import Head from './components/Head.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <Head msg="Basic Form App" />
      <MyForm />
    </div>
  </header>

</template>

<script>
import MyForm from './components/Form.vue';

export default {
  name: 'App',
  components: {
    MyForm
  }
};
</script>