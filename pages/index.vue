<template>
  <div class="wrapper">
    <div class="container">
      <Top />
    </div>
    <main class="main">
      <div class="container">
        <Sidebar />
        <Grid />
      </div>
    </main>
  </div>
</template>

<script>

export default {
    name: "IndexPage"
}
</script>

<style lang="scss">
  body {
    font-family: 'Source Sans Pro', sans-serif;
    background: #E5E5E5;
  }
  .container {
    width: 100%;
    max-width: 1440px;
    margin: auto;
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