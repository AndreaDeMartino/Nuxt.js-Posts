<template>
  <form @submit.prevent="onSave">
    <AppControlInput v-model="editedPost.author"> Author Name </AppControlInput>

    <AppControlInput v-model="editedPost.title"> Title </AppControlInput>

    <AppControlInput v-model="editedPost.thumbnailLink">
      Thumbnail Link
    </AppControlInput>

    <AppControlInput control-type="textarea" v-model="editedPost.content">
      Content
    </AppControlInput>

    <AppButton type="submit">Save</AppButton>

    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel"
    >
      Cancel
    </AppButton>
  </form>
</template>

<script>
import AppControlInput from '@/components/UI/AppControlInput.vue'
import AppButton from '@/components/UI/AppButton.vue'

export default {
  props: {
    post: {
      type: Object,
      required: false,
    },
  },
  components: {
    AppButton,
    AppControlInput,
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : { author: '', title: '', thumbnail: '', content: '' },
    }
  },
  methods: {
    onSave() {
      console.log('Post Saved')
    },
    onCancel() {
      this.$router.push('/admin')
    },
  },
}
</script>

<style scoped></style>
