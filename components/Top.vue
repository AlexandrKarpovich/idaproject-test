<template>
    <div class="top">
      <h2 class="title">Добавление товара</h2>
      <div class="filter">
        <select class="form-select" aria-label="Default select example">
          <option selected>По умолчанию</option>
          <option value="1">One</option>
          <option value="2">Two</option>
          <option value="3">Three</option>
        </select>
      </div>
    </div>
</template>

<script>
export default {
    name: 'Top'
}
</script>

<style lang="scss">
    .top {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .filter {
      select {
        option {

        }
      }
    }
</style>