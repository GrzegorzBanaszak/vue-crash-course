<template>
  <article>
    <CardHeader :balance="345.23" />
    <CardBody />
  </article>
</template>

<script>
import CardHeader from "./CardHeader.vue";
import CardBody from "./CardBody.vue";

export default {
  name: "CardContainer",
  components: {
    CardHeader,
    CardBody,
  },
};
</script>

<style leng="scss" scoped>
article {
  width: 100%;
}
</style>
