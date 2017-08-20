<template>
  <div id="app">
    <img src="./assets/logo.png">
    <child :num="num" @forChildAdd="parnentAdd" @forCHildDecrease="parentDecrase"></child>
    {{num}}
  </div>
</template>

<script>
import child from './components/child.vue';
export default {
  name: 'app',
  data () {
    return {
      num: 15
    };
  },
  components: {
    child
  },
  methods: {
    parnentAdd () {
      this.num++;
    },
    parentDecrase () {
      this.num--;
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
