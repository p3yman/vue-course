<template>
  <div>
    <page-header />
    <h1 style="padding: 50px;">Blog</h1>
    <nuxt />
    <page-footer />
  </div>
</template>

<script>
  import PageHeader from '@/components/layout/Header';
  import PageFooter from '@/components/layout/Footer';

  export default {
    name: 'DefaultLayout',

    components: {
      PageHeader,
      PageFooter,
    },
  }
</script>
