```js
async function getProducts(url) {

    const response = await fetch(url);

    const product = await response.json();
    
    return product;
}

const obj = await getProducts('https://fakestoreapi.com/products');

const products = [0, 3, 0, 5, 4];

let totalPrice = 0;

for(let i = 1; i < products.length; ++i){

    totalPrice += products[i] * obj[i - 1].price;

}

console.log(totalPrice);
```
