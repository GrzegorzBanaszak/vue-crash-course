<template>
  <div class="card__body">
    <h2>Spending - Last 7 days</h2>
    <div class="columns">
      <ColumnItem
        v-for="(item, index) in weeks"
        :key="index"
        :value="item.amount"
        :week="item.day"
        :size="getProcentage(item.amount)"
      />
    </div>
  </div>
</template>

<script>
import ColumnItem from "./ColumnItem.vue";
export default {
  name: "CardBody",
  components: {
    ColumnItem,
  },
  data() {
    return {
      weeks: [
        {
          day: "mon",
          amount: 17.45,
        },
        {
          day: "tue",
          amount: 34.91,
        },
        {
          day: "wed",
          amount: 52.36,
        },
        {
          day: "thu",
          amount: 31.07,
        },
        {
          day: "fri",
          amount: 23.39,
        },
        {
          day: "sat",
          amount: 43.28,
        },
        {
          day: "sun",
          amount: 25.48,
        },
      ],
      maxValue: 0,
    };
  },
  methods: {
    getMax() {
      let max = 0;
      for (let i = 0; i < this.weeks.length; i++) {
        if (max < this.weeks[i].amount) {
          max = this.weeks[i].amount;
        }
      }
      this.maxValue = max;
    },
    getProcentage(vaule) {
      return Math.floor((vaule * 100) / this.maxValue) + "%";
    },
  },
  mounted() {
    this.getMax();
  },
};
</script>

<style lang="scss" scoped>
.card__body {
  margin-top: 1rem;
  background-color: hsl(33, 100%, 98%);
  padding: 2rem 2rem;
  border-radius: 15px;
}

.columns {
  margin-top: 1rem;
  display: flex;
  justify-content: space-evenly;
}
</style>
