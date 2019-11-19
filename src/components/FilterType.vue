<template>
  <div class="filter-type">
    <p>{{filter.name}}</p>
    <div class="img"
      :class="filter.name"
      :style="{ backgroundImage: 'url(' + image + ')' }"
      @click="selectFilter">
    </div> 
  </div>
</template>

<script>
import EventBus from "../js/event-bus";

export default {
  name: "FilterType",
  props: ['filter','image'],
  methods: {
    selectFilter() {
      EventBus.$emit(
       "filter-selected", { filter: this.filter.name }
      );
    }
  }
};
</script>

<style lang="scss" src="../assets/css/filter-type.scss">
// Styles from stylesheet
</style>