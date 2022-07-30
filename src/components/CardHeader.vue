<template>
  <header>
    <div class="header__balance">
      <h4>My balance</h4>
      <p>${{ balance }}</p>
    </div>
    <img src="@/assets/logo.svg" alt="Site Logo" />
  </header>
</template>

<script>
export default {
  name: "CardHeader",
  props: {
    balance: Number,
  },
};
</script>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  background-color: hsl(10, 79%, 65%);
  padding: 2rem 2rem;
  border-radius: 15px;
}
.header__balance {
  color: hsl(27, 66%, 92%);
  p {
    font-size: 2.3rem;
    font-weight: 700;
  }
  h4 {
    font-weight: 400;
  }
}
</style>
