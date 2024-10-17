<!-- eslint-disable vue/multi-word-component-names -->
// eslint-disable-next-line vue/multi-word-component-names
// eslint-disable-next-line vue/multi-word-component-names
<template>
    <div class="products-page">
      <h2><b>Product Management</b></h2>
      <ProductForm @add-product="addProduct" />
      <ProductList :products="products" @edit-product="editProduct" />
    </div>
  </template>
  
  <script>
  import ProductForm from './ProductForm.vue';
  import ProductList from './ProductList.vue';
  
  export default {
    components: {
      ProductForm,
      ProductList
    },
    data() {
      return {
        products: []
      };
    },
    methods: {
      addProduct(product) {
        this.products.push(product);
      },
      editProduct({ index, updatedProduct }) {
        this.$set(this.products, index, updatedProduct);
      }
    }
  };
  </script>
  
  <style scoped>
  .products-page {
    padding: 20px;
    background-color: #f0f0f0;
    min-height: 100vh;
    text-align: center;
  }
  
  h2 {
    color: #333;
  }
  </style>