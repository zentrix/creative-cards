<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-12">
        <nav-header @pageWasChanged="currentPage = $event"></nav-header>
        <components :is="currentPage"></components>
      </div>
    </div>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import CardFront from './components/card/CardFront.vue'
  

  export default {
    data: function(){
      return {
        currentPage: 'cardFront'
      }
    },
    components: {
      navHeader: Header, 
      cardFront: CardFront
    }
  }
</script>

<style>

  body{
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    color: #333;
  }
  a{
    cursor: pointer;
  }
</style>
