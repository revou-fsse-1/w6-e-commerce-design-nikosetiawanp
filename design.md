# E-Commerce Design Assignment

## 1. Given a product id, show the product details

### Sequence Diagram

![Sequence Diagram](/images/sequence-diagram.jpg "Sequence Diagram")

### Algorithm

1. User input product ID
2. Connect to database
3. Query the database for the given ID
4. If product is found, retrieve product details
5. Display the retrieved details back to the user
6. If the product is not found, display error message

### Pseudocode

```pseudocode
function showPrductDetails(productId)
1. Prompt user to enter product ID.
2. Read the product ID input from user.
3. Connect to database, where the details are stored.
4. Query the database for the product with given iD.
5. If the product is found :
    a. retrieve product details.
    b. display the product details to the user.

6. If the product is not found :
    a. Display error message to the user.
```

### Complexity Analysis

The complexity of showProductDetails is O(1), because it only neeed to loop through the database once, to find the given ID, and only have 1 input, which is product ID.

---

## 2. Create Order

### Activity Diagram

![Activity Diagram](/images/activity-diagram.jpg "Activity Diagram")

### Algorithm

1. Retrieve details from user (name, price, quantity, etc.)
2. Calculate total cost
3. Reduce stock level based on the purchased quantity
4. Display total price and product to user

### Pseudocode

```pseudocode
function createOrder(products)
1. Input an array of product objects
2. Initialize totalPrice to 0
3. Loop through each product in the array :
    a. Add the price of the current product to totalPrice
    b. Subtract 1 from the quantity of the current product
4. Return an object containing the totalPrice and updated products
```

### Complexity Analysis

The complexity of createOrder(products) is O(n), because we need to loop through each product in the array. More products mean more loop to do.
