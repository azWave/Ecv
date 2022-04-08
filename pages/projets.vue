<template>
<div>
  <!-- <nuxt-content v-for="page in pages" :key="page.slug"
    :document="page"/> -->
  <nuxt-content :document="page" />
</div>
  
  
</template>

<script>
export default {
  name:"projets",
  async asyncData ({ $content }) {
    const page = await $content('projet').fetch()

    return {
      page
    }
  },
  // async fetch() {
  // const pages = await this.$content("accueil").sortBy('slug', 'asc').fetch()
  // // this.setPages(pages)
  // },
  // methods: {
  //   ...mapActions(['setPages']),
  // },
  // computed: {
  //   ...mapGetters({ pages: 'getPages'}),
  // },
}
</script>

<style>

</style>