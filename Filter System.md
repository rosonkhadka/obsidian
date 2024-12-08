###  Login 
Make a login page, where users can enter the credentials and login and enter the app.
the page should have minimum of two input fields where user can enter his/her username/email and password for logging in 

### Product Index - Show all products
There should be a product page that will list products. 
`'https://dummyjson.com/products'` this is an dummy api that will provide you with a list of 30 products with necessary product details.
Sample response
```json
{ 
	"id": 1, 
	"title": "Essence Mascara Lash Princess", 
	"description": "The Essence Mascara Lash Princess is a popular mascara known for its volumizing and lengthening effects. Achieve dramatic lashes with this long-lasting and cruelty-free formula.", 
	"category": "beauty", 
	"price": 9.99, 
	"discountPercentage": 7.17, 
	"rating": 4.94, 
	"stock": 5, 
	"tags": [ "beauty", "mascara" ], 
	"brand": "Essence", 
	"sku": "RCH45Q1A", 
	"weight": 2, 
	"dimensions": { 
		"width": 23.17, 
		"height": 14.43, 
		"depth": 28.01 
	}, 
	"warrantyInformation": "1 month warranty", 
	"shippingInformation": "Ships in 1 month", 
	"availabilityStatus": "Low Stock", 
	"reviews": [ 
		{ 
			"rating": 2, 
			"comment": "Very unhappy with my purchase!", 
			"date": "2024-05-23T08:56:21.618Z", 
			"reviewerName": "John Doe", 
			"reviewerEmail": "john.doe@x.dummyjson.com" 
		},
		{ 
			"rating": 2, 
			"comment": "Not as described!", 
			"date": "2024-05-23T08:56:21.618Z", 
			"reviewerName": "Nolan Gonzalez", 
			"reviewerEmail": "nolan.gonzalez@x.dummyjson.com" 
		}, 
		{ 
			"rating": 5, 
			"comment": "Very satisfied!", 
			"date": "2024-05-23T08:56:21.618Z", 
			"reviewerName": "Scarlett Wright", 
			"reviewerEmail": "scarlett.wright@x.dummyjson.com" 
		}
	], 
	"returnPolicy": "30 days return policy", 
	"minimumOrderQuantity": 24, 
	"meta": { 
		"createdAt": "2024-05-23T08:56:21.618Z", 
		"updatedAt": "2024-05-23T08:56:21.618Z", 
		"barcode": "9164035109868", 
		"qrCode": "..." 
	}, 
	"thumbnail": "...", 
	"images": ["...", "...", "..."] 
}
```
you can make table for listing products. the table should have following features.
    1. Pagination
        1. skip/offset
        2. Limit
there should be a pagination within the table that will help user to see data from different pages.
for skip and limit there should be options that allow users to change the `limit` and `skip`.of the page.
note: `limit` is number rows of we request from the backend. say `limit=35`, we will bet 35 data from backend. `skip` is number of rows we want to skip. say `skip=5`, then backend will skip the first five rows and will send the rows 5 onwards. you can use the api below for reference.
`'https://dummyjson.com/products?limit=<limit_value>&skip=<skip_value>'`
note: replace `limit_value` and `skip_value` with your values
	2. Search - Via Title, SKU
the product page should have feature for search that will allow user to search for products.
one should be able to search products. the api below will help you perform this.
`'https://dummyjson.com/products/search?q=<search_vale>'`
note: replace search `search_value` with you data to search
	3. Sorting 
there should be ability to sort  products based on certain columns of the table. you dont necessarily  need to sort for all columns. add sort for `title`, `price`,  `rating` and `stock`.  you can use `'https://dummyjson.com/products?sortBy=<column_name>&order=<sort_value>'`
here `column_name` will be the any keys that  are in the response and `sort_value=asc/desc` 
    4. Filter
there should be filter in the  product page. one should be able to filter products based on following attributes.
        1. Category
		2. Price Range
		3. Tags 
		4. Brand
		5. Rating - Range
these filters should be done from frontend. there is no specific api for filtering. however you can use `'https://dummyjson.com/products/category-list'` for fetching categories to show within the category filter.
### Product Show - Show Specific Product
there should be  a page where all the details of a single product will be shown,  including the reviews of the products. you can use `'https://dummyjson.com/products/<product_id>'` to fetch a particular product detail
note: replace `product_id` with actual product id
    1. Product Detail - Everything
    2. Reviews