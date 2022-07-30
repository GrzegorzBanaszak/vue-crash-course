<template>
  <main class="container">
    <CardContainer />
  </main>
</template>

<script>
import CardContainer from "./components/CardContainer.vue";
export default {
  name: "App",
  components: {
    CardContainer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;700&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "DM Sans", sans-serif;
  font-size: 18px;
  background-color: hsl(27, 66%, 92%);
}
.container {
  max-width: 800px;
  margin: 0 auto;
  height: 100vh;
  display: flex;
  align-items: center;
}
</style>
