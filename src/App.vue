<template>
  <div class="apex_parent">

    <delete-button></delete-button>

    <toast-notification></toast-notification>

    <post-button></post-button>

  </div>
</template>

<script>
import DeleteButton from './components/DeleteButton.vue';
import ToastNotification from './components/ToastNotification.vue';
import PostButton from './components/PostButton.vue';
export default {
  name: 'App',
  components: {

    DeleteButton,
    ToastNotification,
    PostButton
  }
}
</script>

<style>

</style>
