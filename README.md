# Desafio 1 :  Clases 

### Run desafio : 
Ejecutar el siguiente comando : 

```sh
node main.js
```

### Diseño del desafio :

Se crea la clase **ProductManager** , la cual contiene los siguientes metodos publicos : 

```
- addProduct
- getProducts
- getProductByid
```
<br>

Existe un metodo privado que sirve de validador del code que se esta intentando guardar con **addProduct**

<br>

```
#validateIdCode
```
Se crea la clase **Product** , la cual contiene los siguientes propiedades:

```
- title, 
- description, 
- price, 
- thumbnail,
- code 
- stock
```
El campo **code** se genera automaticamente de manera incremental a medida que se instancia la clase.Para ello se utilza el metodo static sobre un contador el cual se instancia en el campo **this.code**. 

<br>

```js
export default class Product {
    static #count = 1;

    constructor(title, description, price, thumbnail, stock){
        this.title = title;
        this.description = description;
        this.price = price;
        this.thumbnail = thumbnail;
        this.code = Product.#count++; 
        this.stock = stock 
    }
}
```


