<script>
export default {
    name: "ProductsAndInfo",
    props :[
        "ShopItems"
    ],
data (){

},
methods: {
    logga() {
        console.log("Caricato il componente App, che ha richiamato il metodo 'logga()'");
    },
    getImagePath: function(imgPath) {
        return new URL(imgPath, import.meta.url).href;
    }
},
mounted(){

    }
}
</script>

<template>
    <div v-for="item in ShopItems">
        <p>{{ item.title }}</p>
        <p>{{ item.imgPath }}</p>
        <img :src="'.'+item.imgPath" alt="">
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as*;
*{
    color: white;
}
</style>