<template>
  <section class="posts-list">
    <post-preview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :thumbnail="post.thumbnail"
      :title="post.title"
      :previewText="post.previewText"
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
    posts: {
      type: Array,
      required: true,
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
