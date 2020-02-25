<template>
  <div id="calendar-week" class="container">
    <div class="columns is-mobile">
      <CalendarDay v-for="day in sharedData.seedData" :key="day.id" :day="day" />
    </div>
  </div>
</template>

<script>
import { store } from "../store";
import CalendarDay from "./CalendarDay.vue";

export default {
  name: "CalendarWeek",
  data() {
    return {
      sharedData: store.state
    };
  },
  components: {
    CalendarDay
  }
};
</script>

<style lang="scss" scoped>
#calendar-week {
  margin-bottom: 50px;
  .column {
    padding: 0 0 0 0;
  }

  
}
</style>