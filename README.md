# vue-3-ecommerce

Tienda

## Entities

### Product

- id
- name
- description
- price
- image

### Category

- name
- description

### Cart

- products: `[{productId: 1, quantity: 3},{productId: 7 quantity: 5}]`

## Components

### ProductCard

## Pages

- / -> Todos los productos
- / category/5 -> Productos solo de la categoria 5
- / cart -> Ver el carrito de compras


## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
