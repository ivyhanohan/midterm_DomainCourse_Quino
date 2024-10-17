<template>
    <div class="product-list">
      <h3>Product List</h3>
      <ul v-if="products.length">
        <li v-for="(product, index) in products" :key="index" class="product-item">
          <span v-if="editIndex !== index">
            {{ product.name }} - {{ product.price }} - {{ product.description }}
            <button @click="editProduct(index)">Edit</button>
          </span>
          <span v-else>
            <input v-model="editProductData.name" placeholder="Product Name" />
            <input v-model="editProductData.price" type="number" placeholder="Price" />
            <textarea v-model="editProductData.description" placeholder="Description"></textarea>
            <button @click="saveEdit(index)">Save</button>
          </span>
        </li>
      </ul>
      <p v-else>No products added yet.</p>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      products: Array
    },
    data() {
      return {
        editIndex: -1,
        editProductData: { name: '', price: '', description: '' }
      };
    },
    methods: {
      editProduct(index) {
        this.editIndex = index;
        this.editProductData = { ...this.products[index] };
      },
      saveEdit(index) {
        this.$emit('edit-product', { index, updatedProduct: this.editProductData });
        this.editIndex = -1;
      }
    }
  };
  </script>
  
  <style scoped>
  .product-list {
    margin: 20px auto;
    max-width: 600px;
    background-color: #e383de;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    color: #333;
  }
  
  h3 {
    color: #007bff;
    margin-bottom: 15px;
    text-align: center;
  }
  
  .product-item {
    margin-bottom: 15px;
    padding: 15px;
    background-color: #ffffff;
    border: 1px solid #ddd;
    border-radius: 8px;
    transition: background-color 0.2s ease;
  }
  
  .product-item:hover {
    background-color: #f0f8ff;
  }
  
  button {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 6px 14px;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.2s ease;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  input,
  textarea {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 6px;
    margin-top: 5px;
    background-color: #fafafa;
    color: #333;
    font-size: 1em;
  }
  
  input::placeholder,
  textarea::placeholder {
    color: #999;
  }
  </style>
  