<template>
    <div class="grid">
        <div class="card" v-for="(item, index) in cards" :key="index">
            <Card 
                :title="item.title"
                :descr="item.descr"
                :imgUrl="item.imgUrl"
                :price="item.price"
                />
        </div>
    </div>
</template>

<script>
import Card from './Card.vue';
export default {
    name: "Grid",
    components: { Card },
    props: [],
    data() {
        return {
            cards: [
                {
                    title: 'Наименование товара',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 2',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 3',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 4',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 5',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 6',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                },
                {
                    title: 'Наименование товара 7',
                    descr: "Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк",
                    imgUrl: 'https://raw.githubusercontent.com/AlexandrKarpovich/idaproject-test/master/static/img.jpg',
                    price: 10000
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    .grid {
        // width: 75%;
        max-width: 1280px;
        // margin-left: auto;
        margin-left: 348px;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(265px, 1fr));
        grid-gap: 16px;
        overflow-y: auto;
        padding-top: 8px;
        padding-right: 8px;
    }
</style>