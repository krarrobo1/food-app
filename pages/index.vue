<template>
  <main class="container">
    <AppHeader/>
    <AppRestaurantInfo :dataSource="foodData"/>
  </main>
</template>

<script>
  import AppHeader from '../components/AppHeader.vue';
  import AppRestaurantInfo from '../components/AppRestaurantInfo.vue';
      import { mapState } from 'vuex';

  export default{
      
        computed: {
          ...mapState([
            'foodData',
          ])
        },
      components: {
        AppHeader,
        AppRestaurantInfo
      }
  }
</script>
<style>
  html{
    font-family: "Hulish", -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 300;
  }
  h1, h2, h3, h4{
    font-family: "Poppins", -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 600;
  }
</style>