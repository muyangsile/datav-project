<template>
  <div id="app">
    <DataVComportment/>
  </div>
</template>

<script>
import DataVComportment from './components/DataVComportment.vue';
export default {
  name: 'App',
  components: {
    DataVComportment
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
}
body{
 background: url('@/assets/images/bg.jpg') no-repeat top center;
 background-size: 100% auto;
}
</style>
