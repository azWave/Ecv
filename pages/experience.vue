<template>
<div>
    <nuxt-content v-for="page in pages" :key="page.slug"
    :document="page"/>
</div>
  
</template>

<script>
import{ mapGetters , mapActions} from 'vuex'
export default {
  name:"expereinces",
  async fetch() {
  const pages = await this.$content("experiences").sortBy('slug', 'asc').fetch()
  console.log('coucou')
  this.setPages(pages)
  },
  methods: {
    ...mapActions(['setPages']),
  },
  computed: {
    ...mapGetters({ pages: 'getPages'}),
  },
}
</script>

<style>
.flex{
  display: flex;
}
.flex div{
  width: 40%;
  margin-left: 5%;
  margin-right: 5%;
}

.flex h2{
  text-decoration: underline 5px;
  text-decoration-color: #73A1F8;
}
</style>