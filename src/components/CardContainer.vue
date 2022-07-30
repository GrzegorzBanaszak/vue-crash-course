<template>
  <article>
    <CardHeader />
  </article>
</template>

<script>
import CardHeader from "./CardHeader.vue";
export default {
  name: "CardContainer",
  components: {
    CardHeader,
  },
};
</script>

<style scoped>
article {
  width: 100%;
}
</style>
