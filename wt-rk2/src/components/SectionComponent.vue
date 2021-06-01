<template>
<section class="container" :id="id">
  <div class="section container">
    <div class="section-left">
      <img :src="img" class="section-left__img">
    </div>
    <div class="section-right">
      <h2 class="section-right__heading">{{heading}}</h2>
      <div class="section-right__text">{{content}}</div>
      <ul class="section-right__ul">
        <li class="section-right__li" v-for="(item, key) in list" :key="key">{{item}}</li>
      </ul>
    </div>
  </div>
</section>
</template>

<script>
export default {
  name: "Section",
  props:{
    img: {
      type: Object,
    },
    heading: {
      type: String,
      default: '#'
    },
    content: {
      type: String,
      default: '#'
    },
    list: {
      type: Array,
    },
    id: {
      type: String,
      default: '#'
    }
  }
}
</script>

<style scoped>

</style>