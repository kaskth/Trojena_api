# Feedback API

The Feedback API is a RESTful API that allows users to submit feedback for a product or service. The API enables developers to create applications that can easily accept and manage user feedback, as well as retrieve and analyze feedback data.


| Method | Function |
|-------:|----------|
|   Post | Create   |


## Create

To leave a rating and comment on a product, please log in to your account first. This helps ensure the authenticity and quality of feedback provided by our users. If you don't have an account, you can easily create one by clicking on the 'Sign Up' button on our website.

Post :  https://trojena.oa.r.appspot.com/customer/feedback/create

|  Parameter | Type         | Example   |
|-----------:|--------------|-----------|
| product_id | int          | 1         |
|     rating | decimal(2,1) | 1.5       |
|    message | String       | very good |


Example request:
```
Post /customer/feedback/create
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: Rating added
}
```


