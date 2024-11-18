const productList = [
  {
    name: 'WD 2TB Elements Portable External Hard Drive - USB 3.0',
    description: "USB 3.0 and USB 2.0 Compatibility Fast data transfers Improve PC Performance High Capacity; Compatibility Formatted NTFS for Windows 10, Windows 8.1, Windows 7; Reformatting may be required for other operating systems; Compatibility may vary depending on user's hardware configuration and operating system",
    price: '$65',
    image: "https://fakestoreapi.com/img/61IBBVJvSDL._AC_SY879_.jpg",
  },
  {
    name: 'SanDisk SSD PLUS 1TB Internal SSD - SATA III 6 Gb/s',
    description: "Easy upgrade for faster boot up, shutdown, application load and response (As compared to 5400 RPM SATA 2.5” hard drive; Based on published specifications and internal benchmarking tests using PCMark vantage scores) Boosts burst write performance, making it ideal for typical PC workloads Then perfect balance of performance and reliability Read/write speeds of up to 535MB/s/450MB/s (Based on internal testing; Performance may vary depending upon drive capacity, host device, OS and application.)",
    price: '$ 109',
    image: "https://fakestoreapi.com/img/61U7T1koQqL._AC_SX679_.jpg",
  },
  {
    name: 'Silicon Power 256GB SSD 3D NAND A55 SLC Cache Performance Boost SATA III 2.5',
    description: "3D NAND flash are applied to deliver high transfer speeds Remarkable transfer speeds that enable faster bootup and improved overall system performance. The advanced SLC Cache Technology allows performance boost and longer lifespan 7mm slim design suitable for Ultrabooks and Ultra-slim notebooks. Supports TRIM command, Garbage Collection technology, RAID, and ECC (Error Checking & amp; Correction) to provide the optimized performance and enhanced reliability.",
    image: "https://fakestoreapi.com/img/71kWymZ+c+L._AC_SX679_.jpg",
    price: "$ 109",              
  },
  {
    name: 'Mens Casual Premium Slim Fit T-Shirts',
    description: "Slim-fitting style, contrast raglan long sleeve, three-button henley placket, light weight &amp; soft fabric for breathable and comfortable wearing. And Solid stitched shirts with round neck made for durability and a great fit for casual fashion wear and diehard baseball fans. The Henley style round neckline includes a three-button placket.",
    price: '$ 22.3',
    image: "https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg",
  },
  {
    name: 'Mens Cotton Jacket',
    description: "great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors. Good gift choice for you or your family member. A warm hearted love to Father, husband or son in this thanksgiving or Christmas Day.",
    price: '$ 55.99',
    image: "https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg",
  },
  {
    name: 'Mens Casual Slim Fit',
    description: "The color could be slightly different between on the screen and in practice. / Please note that body builds vary by person, therefore, detailed size information should be reviewed below on the product description.",
    price: '$ 15.99',
    image: "https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg",
  },
  {
    name: "BIYLACLESEN Women's 3-in-1 Snowboard Jacket Winter Coats",
    description: "Note:The Jackets is US standard size, Please choose size as your usual wear Material: 100% Polyester; Detachable Liner Fabric: Warm Fleece. Detachable Functional Liner: Skin Friendly, Lightweigt and Warm.Stand Collar Liner jacket, keep you warm in cold weather. Zippered Pockets: 2 Zippered Hand Pockets, 2 Zippered Pockets on Chest (enough to keep cards or  keys)and 1 Hidden Pocket Inside.Zippered Hand Pockets and  Hidden Pocket keep your things secure. Humanized Design: Adjustable and Detachable Hood and Adjustable cuff to prevent the wind and water,for a comfortable fit. 3 in 1 Detachable Design provide more convenience, you can separate the coat and inner as needed, or wear it together. It is suitable for different season and help you adapt to different climates",
    price: '$ 56.99',
    image: "https://fakestoreapi.com/img/51Y5NI-I5jL._AC_UX679_.jpg",
  },
  {
    name: "Lock and Love Women's Removable Hooded Faux Leather Moto Biker Jacket",
    description: "100% POLYURETHANE(shell) 100% POLYESTER(lining) 75% POLYESTER 25% COTTON (SWEATER), Faux leather material for style and comfort / 2 pockets of front, 2-For-One Hooded denim style faux leather jacket, Button detail on waist / Detail stitching at sides, HAND WASH ONLY / DO NOT BLEACH / LINE DRY / DO NOT IRON",
    price: '$ 29.95',
    image: "https://fakestoreapi.com/img/81XH0e8fefL._AC_UY879_.jpg",
  },
  {
    image: 'https://fakestoreapi.com/img/71HblAHs5xL._AC_UY879_-2.jpg',
    description: "Lightweight perfet for trip or casual wear---Long sleeve with hooded, adjustable drawstring waist design. Button and zipper front closure raincoat, fully stripes Lined and The Raincoat has 2 side pockets are a good size to hold all kinds of things, it covers the hips, and the hood is generous but doesn't overdo it.Attached Cotton Lined Hood with Adjustable Drawstrings give it a real styled look.",
    price: '$ 39.99',
    name: "Rain Jacket Women Windbreaker Striped Climbing Raincoats",
  },
]
const productListElement = document.querySelector(".products--list")

for (let product of productList){
  const listElement= document.createElement('li')
  const divElement= document.createElement('div')
  const imageElement= document.createElement('img')
  const divElement2 = document.createElement('div')
  const productNameElement= document.createElement('h1')
  const productDescriptionElement= document.createElement('p')
  const buttonElement= document.createElement('button')
  const priceElement= document.createElement('p')
  productListElement.appendChild (listElement)
  listElement.appendChild(divElement)
  divElement.classList.add('card');
  divElement.classList.add('product');
  divElement.append(imageElement, divElement2)
  imageElement.src = product.image;
  imageElement.alt = product.name;
  imageElement.classList.add("product--image")
  divElement2.classList.add("product--text")
  divElement2.append(productNameElement, productDescriptionElement, buttonElement, priceElement)
  productNameElement.innerText = product.name;
  productNameElement.classList.add("product--name")
  productDescriptionElement.innerText = product.description;
  productDescriptionElement.classList.add("product--description")
  priceElement.innerText = product.price;
  priceElement.classList.add("product--price")
  buttonElement.innerText = 'Buy Now';
  buttonElement.classList.add("product--buy")






  console.log(product.name, product.description, product.price)
}

// including sorting functionalities

document.addEventListener("DOMContentLoaded",() =>{
const sortDropdwnElement = document.getElementById("sort");
const productListElement = document.querySelector(".products--list");
const products = Array.from(productListElement.children);

  sortDropdwnElement.addEventListener('change', () =>{
    const sortOrder = sortDropdwnElement.value;
    const sortedProducts = products.sort((a,b) =>{
      const priceA = parseFloat(a.querySelector(".product--price").textContent.replace("$", ""));
      const priceB = parseFloat(b.querySelector(".product--price").textContent.replace("$", ""));
      if (sortOrder === "asc"){
        return priceA-priceB;
      }else {
        return priceB-priceA;
      }

    });
    
    // Clear the product list
    while (productListElement.firstChild) {
      productListElement.removeChild(productListElement.firstChild);

    }

     // Append the sorted products
     sortedProducts.forEach((product) =>{
      productListElement.appendChild(product)
     });

  });
});


document.addEventListener("DOMContentLoaded", () => {
const modalCart= document.querySelector("#modalCart");
const cartLink= document.querySelector("#cartLink");
const cartCloseBtn= document.querySelector(".modal-cart-close");
const cartItems= [];
const itemDisplay= document.querySelector(".modal-cart-content p");




cartLink.onclick = function(){
  modalCart.style.display = "block";
  setTimeout(() => {
    modalCart.classList.add("show");
  }, 10);
  
};
cartCloseBtn.onclick = function () {
  modalCart.classList.remove("show");
  setTimeout(() => {
    modalCart.style.display = "none";
   
  }, 300);
};
window.onclick = function (event) {
  if (event.target==modalCart) {
    modalCart.classList.remove("show");
  setTimeout(() => {
    modalCart.style.display="none"
  }, 300);
  }
};






// Cart display section

const addToCartButtons = document.querySelectorAll(".product--buy");
addToCartButtons.forEach((button) => {
  button.addEventListener("click", (event) =>{
    const product = event.target.closest(".product.card");
    const itemName= product.querySelector(".product--name").textContent;
    const itemPrice= product.querySelector(".product--price").textContent;
    
    cartItems.push({
      name: itemName,
      price: itemPrice});

    displayConfirmation(itemName);
    updateCartDisplay();

  });
});

function updateCartDisplay() {
  if (cartItems.length === 0) {
    itemDisplay.textContent = "Your cart is empty.";
  } else {
    itemDisplay.innerHTML =
      "<ul>" +
      cartItems
        .map((item) => `<li>${item.name} - ${item.price}</li>`)
        .join("") +
      "</ul>";
  }
}

function displayConfirmation(itemName) {
  const confirmation = document.createElement("div");
  confirmation.className = "confirmation-message";
  confirmation.textContent = `${itemName} has been added to the cart.`;
  document.body.appendChild(confirmation);

  setTimeout(() => {
    confirmation.remove();
  }, 3000);
}

});
