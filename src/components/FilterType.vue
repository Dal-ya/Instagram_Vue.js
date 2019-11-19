<template>
  <div class="filter-type">
    <p>{{filter.name}}</p>
    <div class="img"
      :class="filter.name"
      :style="{ backgroundImage: 'url(' + image + ')' }">
    </div> 
  </div>
</template>

<script>
export default {
  name: "FilterType",
  props: ['filter','image']
};
</script>

<style lang="scss" src="../assets/css/filter-type.scss">
// Styles from stylesheet
</style>