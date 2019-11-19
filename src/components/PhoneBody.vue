<template>
  <div class="phone-body">
    <div class="feed">
      <vuegram-post
        v-for="post in posts" 
        :post="post"
        :key="posts.indexOf(post)"
      ></vuegram-post>
    </div>
  </div>
</template>

<script>
import VuegramPost from './VuegramPost'

export default {
  name: "PhoneBody",
  props: ['posts','filters'],
  components: {
    VuegramPost
  }
};
</script>

<style lang="scss" src="../assets/css/phone-body.scss">
// Styles from stylesheet
</style>