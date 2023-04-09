# Customer Address.

The Customer Address API is a RESTful API that provides endpoints for managing customer addresses in a database. It allows users to retrieve, create, update, and delete customer addresses.


| Method | Function |
|-------:|----------|
|   Post | Create   |
| Delete | Delete   |


## Create

To add a new address to your profile, authentication is required. Please log in to your account with your credentials before attempting to add a new address.

Post :  https://trojena.oa.r.appspot.com/customer/address/create

|   Parameter | Type   | Example   |
|------------:|--------|------------|
|  country | String |United States  |
| city | String |New York |
|  street | String |123 Main St |
|  building | String   |Apt 4B  |
|  sector | String   |Financial District |
|  phoneNumber | String   |+1 (555) 123-4567 |
|  postNumber | int    |10001 |

Example request:
```
Post /customer/address/create
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: A new address has been added successfully
}
```

## Delete

To remove an existing address from their profile, users must first log in to their account. Once logged in, users can view and manage their profile information, including removing any addresses they no longer wish to keep on file. If the user is not logged in and tries to remove an address from their profile, they will be prompted to log in first.

Delete :  https://trojena.oa.r.appspot.com/customer/address/delete

|   Parameter | Type                | Example   |
|------------:|---------------------|------------|
|  id | int            |1 |

Example request:
```
Delete /customer/address/delete
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: Deleted successfully
}
```

