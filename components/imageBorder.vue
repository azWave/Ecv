<template>
<div class="border">
    <article-image class="image" :src="src" :alt="alt"></article-image>
</div>
    
</template>

<script>
import ArticleImage from './ArticleImage.vue'
export default {
  components: { ArticleImage },
  props: {
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

.border {
  display: inline-block;
  position: relative;
  margin: 1rem 3rem 3rem 1rem;
  z-index: 0;
}

.border::before {
  content: "";
  position: absolute;
  border: 5px solid #73A1F8;
  top: 20px;
  left: 20px;
  width: 450px;
  height: 450px;
  z-index: -1;
}

.image{
    width: 450px;
}
</style>