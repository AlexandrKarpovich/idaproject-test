<template>
    <aside class="sidebar">
        <div class="sidebar__item">
          <label 
            for="name" 
            class="name">Наименование товара
          </label>
          <input 
            type="text" 
            class="form-control is-invalid" 
            id="name" 
            required 
            placeholder="Введите наименование товара"
            v-model.trim="title"
          >
          <p class="invalid">Поле является обязательным</p>
        </div>
        <div class="sidebar__item">
          <label 
            for="exampleFormControlTextarea1" 
            class="form-label">Описание товара
          </label>
          <textarea 
            class="form-control" 
            id="exampleFormControlTextarea1" 
            placeholder="Введите описание товара" 
            rows="3"
            v-model.trim="descr"
            >
          </textarea>
        </div>
        <div class="sidebar__item">
          <label 
            for="name" 
            class="imgUrl">Ссылка на изображение товара
          </label>
          <input 
            type="text" 
            class="form-control is-invalid" 
            id="name" 
            required 
            placeholder="Введите ссылку"
            v-model.trim="imgUrl"
          >
          <p class="invalid">Поле является обязательным</p>
        </div>
        <div class="sidebar__item">
          <label 
            for="name" 
            class="price">Цена товара
          </label>
          <input 
            type="text" 
            class="form-control is-invalid" 
            id="name" 
            required 
            placeholder="Введите цену"
            v-model.trim="price"
          >
          <p class="invalid">Поле является обязательным</p>
        </div>
        <button class="btn" @click="addNewCard">Добавить товар</button>
    </aside>
</template>

<script>
export default {
    name: 'Sidebar',
    data() {
      return {
        title: '',
        descr: '',
        imgUrl: '',
        price: '',
        isValidate: false,
        cards: {}
      }
    },
    methods: {
      addNewCard(event) {
        console.log(this.cards[event.id]);
      },
      // validateInput(value) {
      //   // this.isValidate > value.length < 3
      //   console.log('Validate');
      // }
    }
}
</script>

<style lang="scss">
    .sidebar {
      position: fixed;
      // top: 24px;
      // width: 25%;
      // max-width: 332px;
      // min-width: 230px;
      width: 332px;
      display: flex;
      flex-direction: column;
      box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
      border-radius: 4px;
      padding: 24px;
      box-sizing: border-box;
      margin-top: 8px;

      &__item {
          display: flex;
          flex-direction: column;
          margin-bottom: 16px;
          font-weight: 400;
          font-size: 10px;
          line-height: 13px;
          letter-spacing: -0.02em;
          color: #49485E;
      }
    }
    label {
      width: fit-content;
      display: flex;
      align-items: center;
      padding-right: 5px;
    }
    .name, .imgUrl, .price {
      position: relative;
      &:after {
        content: '';
        position: absolute;
        top: 0;
        right: 0;
        width: 4px;
        height: 4px;
        background: #FF8484;
        border-radius: 4px;
        border-radius: 50%;
        display: flex;
        align-items: center;
      }
    }
    input, textarea {
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
      border-radius: 4px;
      padding: 10px 16px;
      border: none;
      resize: none;
      margin-top: 4px;
      font-weight: 400;
      font-size: 12px;
      line-height: 15px;
      &:placeholder {
        color: #B4B4B4;
      }   
    }
    input.is-invalid {
      border: 1px solid #FF8484;
    }
    .invalid {
      font-weight: 400;
      font-size: 8px;
      line-height: 10px;
      letter-spacing: -0.02em;
      color: #FF8484;
    }
    .btn {
        font-weight: 600;
        font-size: 12px;
        line-height: 15px;
        text-align: center;
        letter-spacing: -0.02em;
        color: #B4B4B4;
        background: #EEEEEE;
        border-radius: 10px;
        padding: 10px;
        border: none;
        cursor: pointer;
    }
</style>