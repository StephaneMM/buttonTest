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
};
</script>

<style scope>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.main {
  display: flex;
}

.img-container {
  margin: 1rem;
}
</style>
