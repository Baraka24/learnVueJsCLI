<template>
    <div class="error-page">
        <img src="https://imgs.search.brave.com/pwudBgp90IvbB7s5BcbobXv3It38eqpsp6aJMcvgOLU/rs:fit:500:0:0/g:ce/aHR0cHM6Ly9zdC5k/ZXBvc2l0cGhvdG9z/LmNvbS8zMzM2MzM5/LzQ2MzMvaS82MDAv/ZGVwb3NpdHBob3Rv/c180NjMzMTI2NS1z/dG9jay1waG90by00/MDQtZXJyb3ItcGFn/ZS1jb25jZXB0LW9m/LmpwZw" alt="404 Page Not Found">
        <h1>Page Not Found</h1>
        <p>The page you are looking for could not be found.</p>
        <router-link to="/">Home</router-link>
    </div>
  </template>
  
  <script>
  export default {
    name: 'NotFound',
    data() {
      return {
        
      }
    }
  }
  </script>
<style>
    body {
      font-family: sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      background-color: #f2f2f2;
    }

    .error-page {
      width: 500px;
      background-color: #fff;
      padding: 20px;
      text-align: center;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    }

    .error-page img {
      width: 100%;
      max-width: 200px;
      margin-bottom: 20px;
    }

    .error-page h1 {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .error-page p {
      font-size: 16px;
      line-height: 1.5;
    }

    .error-page a {
      color: #007bff;
      text-decoration: none;
    }
</style>