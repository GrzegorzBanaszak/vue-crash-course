<template>
  <footer>
    <div class="footer__right">
      <h4>Total this month</h4>
      <p>$456.23</p>
    </div>
    <div class="footer__left">
      <h5>+ 2.4%</h5>
      <p>from last month</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "CardFooter",
};
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  padding-top: 2rem;
  color: hsl(25, 47%, 15%);
}

.footer {
  &__right {
    h4 {
      font-weight: 400;
      color: hsl(28, 10%, 53%);
    }
    p {
      font-size: 3rem;
      font-weight: 700;
    }
  }
  &__left {
    h5 {
      font-weight: 700;
      text-align: right;
      font-size: 1.4rem;
    }
    p {
      font-weight: 400;
      color: hsl(28, 10%, 53%);
    }
  }
}
</style>
