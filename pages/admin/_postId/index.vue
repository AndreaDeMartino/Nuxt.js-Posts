<template>
  <div class="admin-new-post-page">
    <section class="update-form">
      <admin-post-form :post="loadedPost"></admin-post-form>
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm.vue'
export default {
  layout: 'admin',
  components: {
    AdminPostForm,
  },
  data() {
    return {
      loadedPost: {
        author: 'Andrea',
        title: 'My awesome post',
        content: 'Super amazing, thanks for that!',
        thumbnail:
          'https://c7.uihere.com/files/792/139/601/circular-technological-background.jpg',
      },
    }
  },
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
