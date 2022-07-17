<template>
    <div class="grid">
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
       <Card />
    </div>
</template>

<script>
import Card from './Card.vue';
export default {
    name: "Grid",
    components: { Card }
}
</script>

<style lang="scss">
    .grid {
        width: 72%;
        max-width: 1280px;
        margin-left: auto;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
        grid-gap: 16px;
        overflow-y: auto;
        // background: gray;
    }
</style>