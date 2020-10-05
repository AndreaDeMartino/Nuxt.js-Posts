<template>
  <div class="posts-page">
    <post-list :posts="loadedPosts"></post-list>
  </div>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview.vue'
import PostList from '@/components/Posts/PostList.vue'
export default {
  components: {
    PostPreview,
    PostList,
  },
  data() {
    return {
      loadedPosts: [
        {
          id: '1',
          title: 'Hello There',
          previewText: 'This is my first post!',
          thumbnail:
            'https://ak.picdn.net/shutterstock/videos/14597056/thumb/1.jpg',
        },
        {
          id: '2',
          title: 'Hi friends',
          previewText: 'Yeah, this is my second post.',
          thumbnail:
            'https://cdn.pixabay.com/photo/2017/12/26/21/19/tech-3041437_960_720.jpg',
        },
        {
          id: '3',
          title: 'Whats Up guys',
          previewText: 'And This is my third post.',
          thumbnail:
            'https://c7.uihere.com/files/792/139/601/circular-technological-background.jpg',
        },
      ],
    }
  },
}
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
