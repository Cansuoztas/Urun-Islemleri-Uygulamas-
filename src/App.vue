<template>
  <div>
    <app-header></app-header>
    <app-container></app-container>
    <app-footer></app-footer>
  </div>

</template>

<script>
import Header from "./components/shared/Header"
import Footer from "./components/shared/Footer"
import ProductPurchase from "./components/products/ProductPurchase"
import ProductSell from "./components/products/ProductSell"
import ProductList from "./components/products/ProductList"

export default {
  components : {
    appHeader : Header,
    appFooter : Footer,
    appContainer : ProductPurchase,
    appContainer : ProductSell,
    appContainer : ProductList
  }
}

</script>

<style>

</style>
