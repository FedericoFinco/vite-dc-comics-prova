<script>
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import ProductsAndInfo from './components/productsAndInfo.vue'
import MainContent from './components/mainContent.vue'

export default {
  components: {
    AppHeader,
    AppFooter,
    ProductsAndInfo,
    MainContent,
  },
  data() {
    return {
      categoriaProdotti: "LA PASTA",
      DCComicsList: [
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
        "Fans",
        "Shop"
      ],
      ShopItems: [
        {
          title : "Digital Comics",
          imgPath: "./assets/buy-comics-digital-comics.png"
        },
        {
          title : "DC Merchandise",
          imgPath: "./assets/buy-comics-merchandise.png"
        },
        {
          title : "Subscription",
          imgPath: "./assets/buy-comics-subscriptions.png"
        },
        {
          title : "Comic Shop Locator",
          imgPath: "./assets/buy-comics-shop-locator.png"
        },
        {
          title : "DC Power Visa",
          imgPath: "./assets/buy-dc-power-visa.svg"
        }
      ]
    }
  },
  methods: {
    logga() {
      console.log("Caricato il componente App, che ha richiamato il metodo 'logga()'");
    }
  },
  mounted() {
    this.logga();
  }
}
</script>

<template>
<AppHeader :list="DCComicsList" />
<main>
  <MainContent />
  <ProductsAndInfo :ShopItems="ShopItems" />
</main>
<AppFooter />
</template>

<style lang="scss" scoped>
@use './styles/partials/variables.scss' as*;
main{
  background-color: #222;
}
</style>
