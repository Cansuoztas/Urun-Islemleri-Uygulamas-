<template>
  <div class="container">
    <div class="row">
        <div class="col-6 offset-3 pt-3 card mt-5 shadow">
            <div class="card-body">
                <h3>Ürün İşlemleri</h3>
                <hr>
                <div class="form-group">
                    <label>Ürün Adı</label>
                    <input  v-model="product.title" type="text" class="form-control" placeholder="Ürün adını giriniz..">
                </div>
                <div class="form-group">
                    <label>Adet</label>
                    <input v-model="product.count" type="number" class="form-control" placeholder="Ürün adetini giriniz..">
                </div>
                <div class="form-group">
                    <label>Fiyat</label>
                    <input  v-model="product.price" type="number" class="form-control" placeholder="Ürün fiyatı giriniz..">
                </div>
                <div class="form-group">
                    <label>Açıklama</label>
                    <textarea cols="30" rows="5" placeholder="Ürüne ait bir açıklama giriniz..."
                              class="form-control"></textarea>
                </div>
                <hr>
                <button class="btn btn-primary" @click="saveProduct">Kaydet</button>
            </div>
        </div>
    </div>
</div>
</template>
<script>
  export default {
    data(){
      return{
        product : {
          title : "",
          count: null,
          price: null,
          description : ""
        }
      }
    },
    methods:{
      saveProduct(){
        this.$store.dispatch("saveProduct", this.product)
      }
    }
  }
</script>
<style></style>
