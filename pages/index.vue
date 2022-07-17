<template>
  <div class="wrapper">
    <Top />
    <main class="main">
      <Sidebar />
      <Grid />
    </main>
  </div>
</template>

<script>
import Top from '../components/Top.vue';
import Sidebar from '../components/sidebar.vue';
import Grid from '../components/Grid.vue';

export default {
    name: "IndexPage",
    components: { Top, Sidebar, Grid  }
}
</script>

<style lang="scss">
  body {
    font-family: 'Source Sans Pro', sans-serif;
    background: #E5E5E5;
  }
  .wrapper {
    max-width: 100%;
    padding: 32px;
  }
  
  .main {
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
  }
  

  
</style>