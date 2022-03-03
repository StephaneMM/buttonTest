<template>
  <div>
    <button @click="someoneClicked">
      <slot name="right" />
      <p>{{ message }}</p>
      <slot name="left" />
    </button>
  </div>
</template>

<script>
export default {
  name: "Button",

  props: {
    message: {
      default: "",
      type: String,
    },
  },
  methods: {
    someoneClicked() {
      this.$data.isClicked = !this.$data.isClicked;
      this.$emit("someoneClicked");
    },
  },
};
</script>

<style scoped>
button {
  padding: 1rem;
  font-family: Montserrat;
  font-size: 1.125rem;
  font-weight: 800;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: #fff;
  background-color: #00aaee;
  border-radius: 1.25rem;
  border: 0;
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  justify-items: center;
  user-select: none;
  margin: 0.5rem;
}

button:enabled:active {
  transform: scale(0.98) translateY(2px);
  opacity: 0.9;
  transition: transform 0.05s;
}
</style>
