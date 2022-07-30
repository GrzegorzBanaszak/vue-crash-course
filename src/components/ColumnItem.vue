<template>
  <div class="column">
    <div class="column__week">{{ week }}</div>
    <div class="column__size" :style="{ height: size }"></div>
    <span class="column__value">${{ value }}</span>
  </div>
</template>

<script>
export default {
  name: "ColumnItem",
  props: {
    value: Number,
    week: String,
    size: String,
  },
};
</script>

<style lang="scss" scoped>
.column {
  width: calc(100% / 7);
  display: flex;
  flex-direction: column-reverse;
  height: 100%;
  border-bottom: 1px solid #ccc;
  padding-bottom: 2rem;
  height: 350px;

  &__value {
    background-color: hsl(25, 47%, 15%);
    color: white;
    padding: 10px;
    text-align: center;
    font-weight: 700;
    border-radius: 5px;
    margin: 5px;
    display: none;
  }
  &__size {
    background-color: hsl(10, 79%, 65%);
    margin: 0 0.7rem;
    border-radius: 5px;
    margin-top: 44px;
  }
  &__week {
    text-align: center;
  }
  &:hover {
    cursor: pointer;

    .column__value {
      display: block;
    }
    .column__size {
      margin-top: 0rem;
      background-color: hsla(10, 79%, 65%, 0.685);
    }
  }
}
</style>
