<template>
  <div style="padding-top: 100px;">
    <div>Blog list</div>
    <ul>
      <li v-for="post in posts">
        <nuxt-link :to="`/blog/single/${post.slug}`">{{ post.title }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "index",

    data(){
      return {
        posts: [
          {
            title: 'Hello world',
            slug: 'hello',
          },
          {
            title: 'My diary',
            slug: 'diary'
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
