<template>
    <aside class="sidebar">
        <div class="sidebar__item">
          <label for="name" class="name">Наименование товара</label>
          <input type="text" class="form-control" id="name" required placeholder="Введите наименование товара">
        </div>
        <div class="sidebar__item">
          <label for="exampleFormControlTextarea1" class="form-label">Описание товара</label>
          <textarea class="form-control" id="exampleFormControlTextarea1" placeholder="Введите описание товара" rows="3"></textarea>
        </div>
        <div class="sidebar__item">
          <label for="name" class="name">Ссылка на изображение товара</label>
          <input type="text" class="form-control" id="name" required placeholder="Введите ссылку">
        </div>
        <div class="sidebar__item">
          <label for="name" class="name">Цена товара</label>
          <input type="text" class="form-control" id="name" required placeholder="Введите цену">
        </div>
        <button class="btn">Добавить товар</button>
    </aside>
</template>

<script>
export default {
    name: 'sidebar'
}
</script>

<style lang="scss">
    .sidebar {
        position: fixed;
        // top: 24px;
        width: 25%;
        max-width: 332px;
        min-width: 230px;
        display: flex;
        flex-direction: column;
        box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
        border-radius: 4px;
        padding: 24px;
        box-sizing: border-box;

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
        &::placeholder {
           color: #B4B4B4;
        }   
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