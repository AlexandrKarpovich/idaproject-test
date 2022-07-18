<template>
    <div class="top">
      <h2 class="title">Добавление товара</h2>
      <div class="filter">
        <select class="form-select" aria-label="Default select example" v-model="sortIn">
          <option 
            v-for="(item, index) in sort"
            :value="item.value"
            :key="index"
            >
            {{ item.label }}
          </option>
        </select>
      </div>
    </div>
</template>

<script>
export default {
    name: 'Top',
    data() {
      return {
        sortIn: 'default',
        sort: [
          {
            label: 'По умолчанию',
            value: 'default'
          },
          {
            label: 'По цене min',
            value: 'min'
          },
          {
            label: 'По цене max',
            value: 'max'
          },
          {
            label: 'По наименованию',
            value: 'name'
          },
        ]
      }
    }
}
</script>

<style lang="scss">
    .top {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 16px 0 0;
    }
    .filter {
      position: relative;
      .form-select {
        background: #FFFEFB;
        box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
        border-radius: 4px;
        padding: 10px 16px;
        font-weight: 400;
        font-size: 12px;
        line-height: 15px;
        color: #B4B4B4;
        cursor: pointer;
        border: none;

        option {
          // display: none;
          position: absolute;
          top: 100%;
          right: 0;
          left: 0;
          z-index: 999;
          margin: 0 0;
          padding: 0 0;
          list-style: none;
          border: 1px solid #ccc;
          background-color: white;
          box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
        }
      }
    }
</style>