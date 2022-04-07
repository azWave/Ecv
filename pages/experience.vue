<template>
<div>
  <nuxt-content :document="page" />
</div>
  
</template>

<script>
export default {
  name:"contact",
  async asyncData ({ $content }) {
    const page = await $content('experience').fetch()

    return {
      page
    }
  }
}
</script>

<style>

</style>