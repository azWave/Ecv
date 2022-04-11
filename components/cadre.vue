<template>
    <div class="cadre">
        <div>
            <article-image :src="src" :alt="alt" ></article-image>
        </div>
          <div class="text" v-html="content">
        </div>
    </div>
</template>

<script>
import ArticleImage from './ArticleImage.vue'
export default {
  components: { ArticleImage },
  async asyncData ({ $content }) {
    const page = await $content('basket').fetch()
    return {page}
  },
  props: {
    content:{
        type: String,
        required: true,
    },
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    },
  },
  

}
</script>

<style>

.cadres{
    display:flex;
    text-align: center;
    width: 100%;
    padding-top:15px;
}
.cadre{
    color: black;
    width: 100%;
    background-color: white;
    margin-right: 2%;
    margin-left: 2%;
    border-radius: 10% ;
    overflow: hidden;
    box-shadow: 10px  10px 10px #73A1F8 ;
}

.cadre .text{
  text-align: center;
  width: 100%;
}


</style>