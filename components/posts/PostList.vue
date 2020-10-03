<template>
  <section class="posts-list">
    <post-preview
      id="1"
      thumbnail="https://ak.picdn.net/shutterstock/videos/14597056/thumb/1.jpg"
      title="Hello There"
      previewText="This is my first post!"
      :is-admin="isAdmin"
    ></post-preview>

    <post-preview
      id="2"
      thumbnail="https://cdn.pixabay.com/photo/2017/12/26/21/19/tech-3041437_960_720.jpg"
      title="Hi friends"
      previewText="Yeah, this is my second post."
      :is-admin="isAdmin"
    ></post-preview>

    <post-preview
      id="3"
      thumbnail="https://c7.uihere.com/files/792/139/601/circular-technological-background.jpg"
      title="What's Up guys"
      previewText="And This is my third post."
      :is-admin="isAdmin"
    ></post-preview>
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview.vue'
export default {
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    },
  },
  components: {
    PostPreview,
  },
}
</script>

<style scoped>
.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
