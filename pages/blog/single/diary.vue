<template>

  <div>

    <div class="container">

      <h1 style="padding-top: 100px;">{{ postTitle }}</h1>

      <div class="body" v-html="content"></div>

    </div>

  </div>

</template>

<script>
  import Content from '@/md/diary.md';

  export default {
    name: "hello-world",

    data() {
      return {
        postTitle: 'Diary!'
      }
    },

    computed: {
      content() {
        return Content;
      }
    }
  }
</script>

