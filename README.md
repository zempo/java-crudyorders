# java-orders

## Introduction

This is a basic database scheme with customers, orders, and sales agents. This is part two of a two part CRUD application.

## Instructions

Part 1 of this project created the database and read endpoints. See the repository https://github.com/LambdaSchool/java-orders.  

Part 2 of this project finished the CRUD application by adding create, updating, and delete endpoints.  

Expose the following endpoints

* POST /customers/customer - Adds a new customer including any new orders
  * You can use the following as test data
  
```
    {
        "custname": "John",
        "custcity": "Port Angeles",
        "workingarea": "Washington",
        "custcountry": "USA",
        "grade": "1",
        "openingamt": 70000,
        "receiveamt": 7000,
        "paymentamt": 777,
        "outstandingamt": 0,
        "phone": "5555555555",
        "agent": {
        "agentcode": 8
    },
        "orders": [
        {
            "ordamount": 7777,
            "advanceamount": 777,
            "orderdescription": "SOD",
            "payments": [
            {
                "paymentid": 4
            }
            ]
        }
        ]
    }
```

* PUT /customers/customer/{custcode} - Updates the customer based off of custcode. Does not do anything with Orders!
  * You can use the following as test data
  
```
{
        "custname": "Micheal The Great",
        "custcity": "Seattle",
        "workingarea": "Washington",
        "custcountry": "USA",
        "paymentamt": 0,
        "agent": 
        {
            "agentcode": 11
        }
}
```

* DELETE /customers/customer/{custcode} - Deletes the customer based off of custcode
  * this should also delete the orders of that customer


* POST /orders/order
  * You can use the following as test data
```
{
   "ordamount" : 3.21,
   "advanceamount" : 1.23,
   "orderdescription" : "My New Order",
   "customer":
   {
       "custcode":18
   },
   "payments": [
   {
       "paymentid": 4
   }
   ]
}
```


* PUT /orders/order/{ordernum}
  * You can use the following as test data
```
{
   "advanceamount": 0.00,
   "orderdescription": "Best Order Ever"
}
```

* DELETE /orders/order/{ordernum}


## Stretch goals

* DELETE /agents/unassigned/{agentcode} - Deletes an agent if they are not assigned to a customer 

