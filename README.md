# Inventory-Management-System
This is a full stack(MERN) Project.

## Frontend Technology  
* React, Vite, Redux Toolkit, RTK Query, Lazy Suspense, React Hook Form.
* Antd, Tailwind.
* sweetalert, pagination, recharts, react-icons, moment, hot toast etc.
## Backend Technology
* NodeJs, Express, Mongodb, Mongoose, JWT, Cyclic
* User Authentication with JWT token.
* OTP Verification & User Role Management(Future)

## Features

**Functionalities:** 
* Fully Responsive Dashboard.
* Users Can log in, and register.
* You can not delete an item if the item is associated with other items.
* Create, Update, and Delete Brand and See the List of Brands & Search.
* Create, Update, and Delete Category and See the List of Category & Search.
* Create, Update, Delete Products and See the List of Products & Search.
* Brand & Category dropdown linked with Product Create, Update.
* Dynamic Product Management After Purchase/Sale/Purchase Return/Sale Return
* Create, Update, Delete Customer and See the List of Customer & Search.
* Create, Update, Delete Supplier and See the List of Supplier & Search.
* Create, Update, Delete Expense Type and See the List of Expense Type & Search.
* Create, Update, Delete Expense  and See the list of Expense list & Search.
* Expense Type dropdown linked with Expense Create, Update. 
* In Create method user can add to cart from product dropdown, select quantity based on stock, set price or remove from cart . 
* Create, Update, Delete, Purchase, Details and See the List of Purchase & Search
* Supplier, Product Cart Linked with Purchase & also search by Supplier Name.
* In Create method user can add to cart from product dropdown, select quantity based on stock, set price or remove from cart . 
* Create, Update, Delete, Sale, Details and See the List of Sale & Search
* Customer, Product Cart Linked with Sale & also search by Customer Name.
* In Create method user can add to cart from product dropdown, select quantity based on stock, set price or remove from cart . 
* Create, Update, Delete, Sale Return, Details and See the List of Sale Return & Search
Customer, Product Cart Linked with Sale Return & also search by Customer Name.
* In Create method user can add to cart from product dropdown, select quantity based on stock, set price or remove from cart . 
* Create, Update, Delete, Sale, Details and See the List of Purchase Return & Search
Supplier, Product Cart Linked with Purchase Return & also search by Supplier Name.
* In Create method user can add to cart from product dropdown, select quantity based on stock, set price or remove from cart . 
* Download Purchase, Sale Report as xls/csv etc by Date.
* Can see Purchase, Sale, Return Chart
* Can see total Purchase, Sale, Return, Expense.
		
## Future Update: 
* Will Add User Management with Role.
Forget Password, OTP Verification, Email Verification.
* Updating the existing globa error handling middleware(currently studying). 
* Implement Logger(Winston) for better error tracking, details log(currently studying)currently studying
* Purchase/Sale/Return Update feature.(very soon)
Transaction rollback method where needed.(very soon)
* Advance RTK Query Caching for better data fetching in frontend.
## Challanges
```
* Designing the database schema for Purchase, Sale, and Return was challenging for me since it was my first experience with such a large-scale application. Although I had completed an advanced Backend course that included a module on database design, it took me about 10-15 days to analyze the requirements and create the schema.

* During the project, I had to make multiple changes to the schema design. Since there was no dedicated project architect or manager, I had to handle everything myself. The CEO continuously added, edited, or removed requirements and designs throughout the project.

* These ongoing changes required me to frequently adjust the schema design to meet the evolving project needs. Despite the challenges, I managed to navigate through the modifications and ensure that the final database schema met the updated requirements by the end of the project.

* Dynamic product management in Purchase, Sale & Return Controller: When the user creates new Purchase/sale Return Stock product will increase dynamically. Other hand for Sale & Purchase Return stock will decrease. Every Purchase/Sale/Return can have multiple products and increase/decrease them.

* Purchase, Sale, Return Details using multi-stage aggregation pipeline with $lookup operator: Yes. $lookup operator is very powerful. I need to show the purchase details. it was easy with $match. But I need the purchase product list in the purchase product collection!!! Again problem comes Co-founder told me to show up the product details. Multiple products with individual Product Name, Category, and Brand !!! Ater 2 days study the aggregation framework and MongoDB operator and with the help of chatgpt I found $push !!!!  first $match the purchase=> lookup the products=> lookup the Brand=> lookup the Category then $group purchase then inside the group $push the products come from lookup.
```
