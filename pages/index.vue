<template>
  <section class="container">
    <div>
      <logo />
      <h2>{{ title }}</h2>
      <p>{{ body }}</p>
      <p v-if="showText">Lorem ipsum dolor sit amet, consectetur adipisicing elit. A alias aliquid aspernatur beatae culpa cupiditate eveniet fugiat magnam maiores minima molestiae mollitia officia quasi quidem similique soluta unde, vitae. Aspernatur?</p>

      <div v-for="post in posts">
        <h2>{{ post.title }}</h2>
        <p>{{ post.body }}</p>
        <hr>
      </div>

      <button class="btn btn-primary" @click="toggleText">Test Button</button>

      <h2 class="subtitle">
        My cat&#39;s pajamas Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  name: 'Index',
  components: {
    Logo
  },

  data() {
    return {
      title: 'My post title',
      body: 'lorem ipsum',
      img: 'images/1.png',
      showText: false,
      posts: [
        {
          title: 'Post title',
          body: 'Content',
        },
        {
          title: 'Another post title',
          body: 'Another ontent',
        }
      ]
    }
  },

  computed: {
    theTitle(){
      return this.title + ' Another'
    }
  },

  beforeCreate() {
    console.log('Here');
  },

  methods: {

    sayHi() {
      alert('Hi!');
    },

    changeTitle() {
      this.title = 'Not my post title'
    },

    toggleText() {
      this.showText = !this.showText;
    },

  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
