<template>
  <div class="lorem">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Id voluptatibus,
      aperiam inventore amet atque vel, culpa fuga, neque rem aliquam porro quos
      accusantium debitis veniam pariatur laudantium! Vitae, ab id?
    </p>
  </div>
</template>

<script>
export default {
  name: "LoremIpsum",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.lorem {
  display: flex;
  flex-direction: row;
  max-width: 20rem;
  border-radius: 1rem;
  box-shadow: 0 5px 20px 0 rgba(0, 0, 0, 0.1);
  background-color: #fff;
  height: fit-content;
  margin: 1rem;
}
</style>
