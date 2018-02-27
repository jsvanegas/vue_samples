<template>
  <li>
    <span class="animal" v-html="icon" @click="toggleDescription"></span>
    <span class="description" v-show="showDescription">{{description}}</span>
  </li>
</template>
<script>
  export default {
    props:['animal', 'description', 'icon'],
    data(){
      return {
        showDescription:false
      }
    },
    methods:{
      toggleDescription(){
          this.showDescription = !this.showDescription
      }
    }
  }
</script>
<style>
  .animal{
    cursor: pointer;
  }
</style>
