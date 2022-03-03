<template>
  <div id="app">
    <Button @someoneClicked="someoneClicked" message="Hej" />
  </div>
</template>

<script>
import Button from "./components/Button/Button.vue";

export default {
  name: "App",
  components: {
    Button,
  },
  methods: {
    someoneClicked() {
      console.log("someoneClicked");
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
