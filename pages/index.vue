<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>
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
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
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
        })
      }, 1000)
    }).then((data) => {
          return data
        }).catch((err) => {
          context.error(err);
        })
  },
}
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
</style>
