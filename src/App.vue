<template>
  <div id="app">
    <Button @someoneClicked="someoneClicked" message="Hej">
      <Icon v-if="isClicked" slot="left" />
      <Icon v-if="isClicked" slot="right" />
    </Button>
  </div>
</template>

<script>
import Button from "./components/Button/Button.vue";
import Icon from "./components/Icon/Icon.vue";

export default {
  name: "App",

  data: () => ({
    isClicked: false,
  }),

  components: {
    Button,
    Icon,
  },

  methods: {
    someoneClicked() {
      this.$data.isClicked = !this.$data.isClicked;
      this.$emit("someoneClicked");
    },
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
