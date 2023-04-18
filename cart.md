# Cart API 

The Cart API is a RESTful API that allows users to manage their shopping carts for an online store. The API enables users to add, remove, update, and view items in their carts.

The Cart API is designed to be simple and intuitive, with straightforward endpoints and clear documentation. It is built using modern technologies and follows best practices for API development, including input validation, error handling, and security measures.

| Method | Function              |
|-------:|-----------------------|
|    Get | read-all              |
|   Post | addition              |
| Delete | removal               |
|  PATCH | increase-the-quantity |
|  PATCH | reduce-the-quantity   |

## Read All

To read all the products in the shopping cart, the customer must log in first.

Post :  https://trojena.oa.r.appspot.com/customer/cart/read-all

|              Parameter | 
|-----------------------:|
|  There is no Parameter |


Example request:
```
Get /customer/cart/read-all
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

[
    {
       data ........
    },
    {
       data ........
    }
]
```


## Addition

To add items to the cart, users must first log in to their account. Once logged in, users can browse the available products and add mint to their cart. The cart will keep track of the quantity and total price of the items. If the user is not logged in and tries to add mint to the cart, they will be prompted to log in first.

Post :  https://trojena.oa.r.appspot.com/customer/cart/addition

|   Parameter | Type                  | Example         |
|------------:|-----------------------|-----------------|
|  product_id | int              | 1               |


Example request:
```
Post /customer/cart/addition
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: Added to cart successfully
}
```

## Removal

To remove items from the cart, users must first log in to their account. Once logged in, users can view the items in their cart and remove any products they no longer wish to purchase. If the user is not logged in and tries to remove a product from the cart, they will be prompted to log in first.

Delete :  https://trojena.oa.r.appspot.com/customer/cart/removal

|   Parameter | Type                  | Example |
|------------:|-----------------------|---------|
|  product_id | int              | 1       |

Example request:
```
Post /customer/cart/removal
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: Removed from cart
}
```

## Increase-the-quantity

To increase the quantity of an item in the shopping cart, users must first log in to their account. Once logged in, users can view the items in their cart and increase the quantity of any products they wish to purchase more of. If the user is not logged in and tries to increase the quantity of an item in the cart, they will be prompted to log in first.

PATCH :  https://trojena.oa.r.appspot.com/customer/cart/increase-the-quantity

|   Parameter | Type                   | Example |
|------------:|------------------------|---------|
|  product_id | int               | 1       |

Example request:
```
Post /customer/cart/increase-the-quantity
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: The quantity has been increased by 1
}
```

## Reduce-the-quantity
To decrease the quantity of a product in the shopping cart by one, users must first log in to their account. Once logged in, users can view the items in their cart and decrease the quantity of any products they wish to purchase less of. If the quantity of a product is reduced to zero, it will be automatically removed from the cart. If the user is not logged in and tries to decrease the quantity of a product in the cart, they will be prompted to log in first.

PATCH :  https://trojena.oa.r.appspot.com/customer/cart/reduce-the-quantity

|   Parameter | Type             | Example |
|------------:|------------------|---------|
|  product_id | int              | 1       |

Example request:
```
Post /customer/cart/increase-the-quantity
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: The quantity has been reduced by 1
}
```
