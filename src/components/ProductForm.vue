<template>
    <div class="product-form">
      <h3>Add a New Product</h3>
      <form @submit.prevent="submitProduct">
        <div class="form-group">
          <label for="name">Product Name:</label>
          <input v-model="product.name" id="name" required />
        </div>
  
        <div class="form-group">
          <label for="price">Product Price:</label>
          <input v-model="product.price" id="price" type="number" required />
        </div>
  
        <div class="form-group">
          <label for="description">Product Description:</label>
          <textarea v-model="product.description" id="description" required></textarea>
        </div>
  
        <button type="submit">Add Product</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        product: {
          name: '',
          price: null,
          description: ''
        }
      };
    },
    methods: {
      submitProduct() {
        this.$emit('add-product', { ...this.product });
        this.product = { name: '', price: null, description: '' };
      }
    }
  };
  </script>
  
  <style scoped>
  .product-form {
    background-color: #d1ebb8;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 3px 12px rgba(0, 0, 0, 0.1);
    max-width: 450px;
    margin: 30px auto;
  }
  
  h3 {
    font-size: 1.5em;
    color: #007bff;
    margin-bottom: 15px;
    text-align: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  
  .form-group {
    margin-bottom: 15px;
  }
  
  input,
  textarea {
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    border: 1px solid #ddd;
    border-radius: 6px;
    background-color: #f7f7f7;
    font-size: 1em;
    color: #333;
  }
  
  input::placeholder,
  textarea::placeholder {
    color: #aaa;
  }
  
  button {
    width: 100%;
    padding: 10px 0;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 6px;
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.2s ease;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  </style>
  