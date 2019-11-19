<template>
  <div class="phone-body">
    <div v-if="step === 1" class="feed">
      <vuegram-post
        v-for="post in posts" 
        :post="post"
        :key="posts.indexOf(post)"
      ></vuegram-post>
    </div>
    <div v-if="step === 2">
      <div class="selected-image"
        :style="{ backgroundImage: 'url(' + image + ')' }"
        :class="selectedFilter">
      </div>  
      <div class="filter-container">
        <filter-type v-for="filter in filters"
          :filter="filter"
          :image="image"
          :key="filters.indexOf(filter)">
        </filter-type>
      </div>
    </div>
  </div>
</template>

<script>
import VuegramPost from './VuegramPost'
import FilterType from './FilterType'

export default {
  name: "PhoneBody",
  props: ['posts','filters','step', 'image', 'selectedFilter'],
  components: {
    VuegramPost,
    FilterType
  }
};
</script>

<style lang="scss" src="../assets/css/phone-body.scss">
// Styles from stylesheet
</style>