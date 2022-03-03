<template>
  <div id="app">
    <div class="main">
      <LoremIpsum />
      <div v-if="isClicked" class="img-container">
        <img
          src="search-svgrepo-com.svg"
          alt="search icon"
          width="50"
          height="60"
        />
      </div>
    </div>

    <Button @someoneClicked="someoneClicked" message="Hej" />
  </div>
</template>

<script>
import Button from "./components/Button/Button.vue";
import LoremIpsum from "./components/LoremIpsum/LoremIpsum.vue";

export default {
  name: "App",

  components: {
    Button,
    LoremIpsum,
  },
  data: () => ({
    isClicked: false,
  }),
  methods: {
    someoneClicked() {
      console.log("someoneClicked");
      this.$data.isClicked = true;
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
