<template>
<div>
    <nuxt-content v-for="page in pages" :key="page.slug"
    :document="page"/>
</div>
  
</template>

<script>
import{ mapGetters , mapActions} from 'vuex'
export default {
  name:"accueil",
  async fetch() {
  const pages = await this.$content("accueil").sortBy('slug', 'asc').fetch()
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
#jeSuis{
  margin-top: 30vh;
  margin-bottom: 150px;
  margin-left: 12%;
  font-size: 50px;
  height: 75vh ;
}
#jeSuis h2{
  margin: 0%;
  color: #6a6a6a;
}
#jeSuis h1{
  margin:0%;
  text-transform: uppercase;
  display: inline;
}
#jeSuis h3{
  text-transform: uppercase;
  color: #73A1F8;
  display: inline;
}
</style>