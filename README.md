# Luiz-Felipe
Corinthians Store
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Corinthians Store</title>
<style>
body {
font-family: Arial, sans-serif;
margin: 0;
padding: 0;
}

header {
background-color: #000000;
color: White;
padding: 15px;
text-align: center;
}

nav a {
color: White;
margin: 0 15px;
text-decoration: none;
}

.produto {
border: 1px solid #ccc;
margin: 10px;
padding: 10px;
display: inline-block;
text-align: center;
}

footer {
text-align: center;
padding: 10px;
background-color: #f4f4f4;
position: relative;
bottom: 0;
width: 100%;
}
</style>
</head>
<body>

<!-- Página Inicial -->
<header>
<h1>CORINTHIANS STORE</h1>
<nav>
<a href="#produtos">Camisas</a>
<a href="#carrinho">Produtos Pro edition</a>
<a href="#carrinho">Carrinho</a>
</nav>
</header>
<main>
<h2>Explore nossos produtos originais e qualificados!</h2>
<p>Oferecemos um produto de alta qualidade.</p>
</main>

<!-- Página de Produtos -->
<section id="produtos">
<h1>Produtos à disposição</h1>
<div class="produto">
<img src="https://imgnike-a.akamaihd.net/strapi/nike/3_e8ba00c547/3_e8ba00c547.png" =AOvVaw2Mfz8BET6iKux5E5Avs80N&ust=1733310836946000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCJCMxJq8i4oDFQAAAAAdAAAAABAk"Camisa do Corinthians preta 2024">
<h3>Camisa do Corinthians preta 2024</h3>
<p>Preço: R$ 550,00</p>
<input type="number" id="quantidade1" min="1" value="1">
<button onclick="adicionarAoCarrinho('Produto 1', 10, quantidade1.value)">Adicionar ao Carrinho</button>
</div>
<div class="produto">
<img src="https://static.zattini.com.br/produtos/testeira-faixa-corinthians-memphis-depay-licenciada-oficial/14/D37-0040-014/D37-0040-014_zoom2.jpg?ts=1729000580?ims=400x" alt="Faixa Jogador Pro">
<h3>Faixa Jogador Pro</h3>
<p>Preço: R$ 95,00</p>
<input type="number" id="quantidade2" min="1" value="1">
<button onclick="adicionarAoCarrinho('Produto 2', 15, quantidade2.value)">Adicionar ao Carrinho</button>
</div>
</section>

<!-- Página do Carrinho -->
<section id="carrinho">
<h1>Carrinho de Compras</h1>
<h2>Itens no Carrinho:</h2>
<div id="carrinhoDiv"></div>
<button onclick="finalizarCompra()">Finalizar Compra</button>
</section>

<footer>
<p>&copy; 2024 Corinthians Store</p>
</footer>

<script>
let carrinho = [];

function adicionarAoCarrinho(nome, preco, quantidade) {
const item = { nome, preco, quantidade: parseInt(quantidade) };
carrinho.push(item);
alert(`${quantidade} ${nome}(s) adicionado(s) ao carrinho!`);
mostrarCarrinho();
}

function mostrarCarrinho() {
const carrinhoDiv = document.getElementById('carrinhoDiv');
carrinhoDiv.innerHTML = '';
let total = 0;

carrinho.forEach(item => {
const totalItem = item.preco * item.quantidade;
total += totalItem;
carrinhoDiv.innerHTML += `<p>${item.quantidade} x ${item.nome} - R$ ${totalItem.toFixed(2)}</p>`;
});

carrinhoDiv.innerHTML += `<h3>Total: R$ ${total.toFixed(2)}</h3>`;
}

function finalizarCompra() {
alert('Compra finalizada com sucesso!');
carrinho = [];
mostrarCarrinho();
}

document.addEventListener('DOMContentLoaded', mostrarCarrinho);
</script>

</body>
</html>
