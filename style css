const productsData = [
  { name: "Rouge à lèvres", price: 15, category: "lips", img: "https://via.placeholder.com/200" },
  { name: "Gloss", price: 12, category: "lips", img: "https://via.placeholder.com/200" },
  { name: "Blush", price: 18, category: "face", img: "https://via.placeholder.com/200" },
  { name: "Fond de teint", price: 25, category: "face", img: "https://via.placeholder.com/200" },
  { name: "Anticerne", price: 14, category: "face", img: "https://via.placeholder.com/200" },
  { name: "Mascara", price: 16, category: "eyes", img: "https://via.placeholder.com/200" }
];

const productsContainer = document.getElementById("products");
const cartItems = document.getElementById("cart-items");
const cartTotal = document.getElementById("cart-total");

let cart = [];

function displayProducts(list) {
  productsContainer.innerHTML = "";
  list.forEach(product => {
    productsContainer.innerHTML += `
      <div class="product">
        <img src="${product.img}" alt="${product.name}">
        <h3>${product.name}</h3>
        <p>${product.price} €</p>
        <button onclick="addToCart('${product.name}', ${product.price})">
          Ajouter au panier
        </button>
      </div>
    `;
  });
}

function filterProducts(category) {
  if (category === "all") {
    displayProducts(productsData);
  } else {
    displayProducts(productsData.filter(p => p.category === category));
  }
}

function addToCart(name, price) {
  cart.push({ name, price });
  updateCart();
}

function updateCart() {
  cartItems.innerHTML = "";
  let total = 0;
  cart.forEach(item => {
    total += item.price;
    cartItems.innerHTML += `<li>${item.name} - ${item.price} €</li>`;
  });
  cartTotal.textContent = "Total : " + total + " €";
}

displayProducts(productsData);
