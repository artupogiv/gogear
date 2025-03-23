# GoGear

GoGear is an e-commerce personal project dedicated to support your tech experience.
[GoGear](https://gogear.artupogiv.com)

## Links

- Website/Frontend: <https://gogear.artupogiv.com>
  - Backend: <https://gogear-api.artupogiv.com>
- Repositories:
  - General: <https://github.com/artupogiv/gogear>
  - Frontend: <https://github.com/artupogiv/gogear-web>
  - Backend: <https://github.com/artupogiv/gogear-api>

Inspirations:

- <https://kiys.chianyung.dev>
- <https://tenjin.style>

## Features

- Home page
  - Hero section
  - Products catalogue
- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item
  - Link: continue shopping, go to products catalogue
  - Link: checkout
- Checkout page
  - Order summary
    - Product items to buy
    - Grand total of all product items to buy
  - Shipping address form
    Name, email, phone, address, province, city, postal code
- Place order / transaction is being processed

## REST API Endpoints

- Production: `https://gogear.artupogiv.com`
- Local: `http://localhost:3000`

| Endpoint         | HTTP     | Description               |
| ---------------- | -------- | ------------------------- |
| `/products`      | `GET`    | Get all products          |
| `/products/:id`  | `GET`    | Get product by id         |
| `/products/seed` | `POST`   | Seed all initial products |
| `/products`      | `POST`   | Add new product           |
| `/products`      | `DELETE` | Delete all products       |
| `/products/:id`  | `DELETE` | Delete product by id      |
| `/products/:id`  | `PUT`    | Update product by id      |

more endopoints later

### Product

```json
{
  "id": "ULID123",
  "name": "Keychron Keyboard Wireless",
  "series": "Q1 HE QMK",
  "price": 3600000
}
```

### Add New Product

Request Body:

```json
{
  "name": "Logitech Mouse Wireless",
  "series": "MX Master 3S",
  "price": 1600000
}
```

Response Body:

```json
{
  "id": "abc123",
  "name": "Logitech Mouse Wireless",
  "series": "MX Master 3S",
  "price": 1600000
}
```