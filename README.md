<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Mini Delivery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #000;
      color: #fff;
    }

    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }

    header {
      background-color: #000;
      padding: 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 24px;
      color: #fff;
    }

    .cover {
      background-image: url("delivery_cover.jpg");
      background-size: cover;
      background-position: center;
      height: 400px;
    }

    .cover-text {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100%;
      padding: 20px;
      background-color: rgba(0, 0, 0, 0.5);
      color: #fff;
      text-align: center;
    }

    .cover-text h2 {
      margin: 0;
      font-size: 32px;
      margin-bottom: 10px;
    }

    .cover-text p {
      margin: 0;
      font-size: 18px;
      font-family: Arial, sans-serif;
    }

    .product {
      margin: 20px;
      padding: 20px;
      background-color: #222;
      border-radius: 5px;
    }

    .product img {
      width: 200px;
      height: 200px;
      object-fit: cover;
      margin-bottom: 10px;
    }

    .product h3 {
      margin: 0;
      font-size: 20px;
      color: #fff;
    }

    .product p {
      margin: 0;
      font-size: 16px;
      color: #fff;
      font-family: Arial, sans-serif;
    }

    footer {
      background-color: #000;
      padding: 20px;
      text-align: center;
    }

    footer p {
      margin: 0;
      font-size: 14px;
      color: #fff;
    }
  </style>
</head>
<body>
  <header>
    <h1>Mini Delivery</h1>
  </header>

  <div class="container">
    <div class="cover">
      <div class="cover-text">
        <h2>Bem-vindo à Mini Delivery!</h2>
        <p>Faça seu pedido e entregaremos na sua porta.</p>
        <button>Ver Cardápio</button>
      </div>
    </div>

    <div class="product">
      <img src="product1.jpg" alt="Produto 1">
      <h3>Produto 1</h3>
      <p>R$ 10.99</p>
    </div>

    <div class="product">
      <img src="product2.jpg" alt="Produto 2">
      <h3>Produto 2</h3>
      <p>R$ 19.99</p>
    </div>

    <div class="product">m      <img src="product3.jpg" alt="Produto 3">
      <h3>Produto 3</h3>
      <p>R$ 7.99</p>
    </div>
  </div>

  <footer>
    <p>&copy; 2023 Mini Delivery. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
