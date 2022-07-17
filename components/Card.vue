<template>
    <div class="card">
        <div>
            <img src="../static/img.jpg" class="card-img-top" alt="" >
        </div>
        
        <div class="card__text">
            <h5 class="card__title">Наименование товара</h5>
            <p class="card__descr">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <span class="card__price">10 000 руб.</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card'
}
</script>

<style lang="scss" scoped>
    .card {
        img {
            width: 100%;
        }
        &__text {
            padding: 16px;
        }
        &__title {
            font-weight: 600;
            font-size: 20px;
            line-height: 25px;
            color: #3F3F3F;
        }
        &__descr {
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #3F3F3F;
        }
        &__price {
            font-weight: 600;
            font-size: 24px;
            line-height: 30px;
            color: #3F3F3F;

        }
    }
</style>