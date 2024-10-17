<!-- <template>
    <div class="home-container">
      <p class="name">Ivy Quino</p>
      <p class="program">Program: BSIT-3</p>
      <nav class="navigation">
        <router-link to="/" class="nav-link">Home</router-link>
        <router-link to="/products" class="nav-link">Products</router-link>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Home'
  };
  </script>
  
  <style scoped>
  .home-container {
    background-color: #333;
    color: #f0f0f0;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .name {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .program {
    font-size: 18px;
    margin-bottom: 20px;
  }
  
  .navigation {
    display: flex;
    gap: 15px;
  }
  
  .nav-link {
    color: #ffffff;
    text-decoration: none;
    padding: 10px 15px;
    background-color: #444;
    border-radius: 5px;
    transition: background-color 0.3s ease;
  }
  
  .nav-link:hover {
    background-color: #555;
  }
  </style> -->

  <template>
    <div class="home-container">
      <p class="name">Ivy Quino</p>
      <p class="program">Program: BSIT-3</p>
      <nav class="navigation">
        <router-link to="/" class="nav-link">Home</router-link>
        <router-link to="/products" class="nav-link">Products</router-link>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Home'
  };
  </script>
  
  <style scoped>
  .home-container {
    background-color:peachpuff;
    color: #333;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    text-align: center;
    max-width: 400px;
    margin: auto;
  }
  
  .name {
    font-size: 28px;
    font-weight: 600;
    color: #007bff;
    margin-bottom: 8px;
  }
  
  .program {
    font-size: 20px;
    color: #555;
    margin-bottom: 25px;
  }
  
  .navigation {
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  
  .nav-link {
    color: #333;
    text-decoration: none;
    padding: 8px 18px;
    border-radius: 6px;
    background-color: #e0e0e0;
    transition: all 0.3s ease;
    font-weight: 500;
  }
  
  .nav-link:hover {
    background-color: #d4d4d4;
    color: #007bff;
  }
  </style>
  