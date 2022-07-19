<template>
    <div class="card__inner">
        <span class="del"></span>
        <div>
            <img
                :src="imgUrl"
                class="card-img-top"
                :alt="imgUrl"
            >
        </div>

        <div class="card__text">
            <h5 class="card__title">{{ title }}</h5>
            <p class="card__descr">{{ descr }}</p>
            <span class="card__price">{{ price }} руб.</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        title: {
            type: String,
            // validator(value) {
            //     return value.length < 3
            // },
            required: true
        },
        descr: {
            type: String,
        },
        imgUrl: {
            type: String,
            default: 'https://media.istockphoto.com/vectors/no-image-available-sign-vector-id922962354?k=20&m=922962354&s=612x612&w=0&h=f-9tPXlFXtz9vg_-WonCXKCdBuPUevOBkp3DQ-i0xqo=',
            // validator(value) {
            //     return value.length < 3
            // },
            required: true
        },
        price: {
            type: Number,
            // validator(value) {
            //     return value.length < 3
            // },
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
    .card {
        &__inner {
            position: relative;
            &:hover {
                .del {
                    cursor: pointer;
                    &:after {
                        content: '';
                        position: absolute;
                        top: -8px;
                        right: -8px;
                        width: 32px;
                        height: 32px;
                        background: #FF8484 url('../static/del.svg') center no-repeat;
                        box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
                        border-radius: 10px;
                        cursor: pointer;
                    }
                }
            }
        }

        img {
            width: 100%;
        }
        &__text {
            padding: 16px;
            background: #FFFEFB;
        }
        &__title {
            font-weight: 600;
            font-size: 20px;
            line-height: 25px;
            color: #3F3F3F;
            margin: 0;
        }
        &__descr {
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #3F3F3F;
            margin-top: 16px;
            margin-bottom: 32px;
        }
        &__price {
            font-weight: 600;
            font-size: 24px;
            line-height: 30px;
            color: #3F3F3F;

        }
    }
</style>
