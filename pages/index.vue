<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>

    <section class="featured-posts">
      <post-preview
        id="1"
        thumbnail="https://ak.picdn.net/shutterstock/videos/14597056/thumb/1.jpg"
        title="Hello There"
        previewText="This is my first post!"
      ></post-preview>

      <post-preview
        id="2"
        thumbnail="https://cdn.pixabay.com/photo/2017/12/26/21/19/tech-3041437_960_720.jpg"
        title="Hi friends"
        previewText="This is my second post!"
      ></post-preview>

      <post-preview
        id="3"
        thumbnail="https://c7.uihere.com/files/792/139/601/circular-technological-background.jpg"
        title="What's Up guys"
        previewText="This is my third post!"
      ></post-preview>
    </section>
  </div>
</template>

<script>
import PostPreview from '@/components/posts/PostPreview.vue'
export default {
  components: {
    PostPreview,
  },
}
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
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

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
