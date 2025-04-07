# Real-time Flipkart API 🛒🚀
The Real-time Flipkart API provides access to Flipkart's product category structure and metadata in real-time. This powerful tool allows developers to integrate Flipkart's extensive product catalog into their applications, websites, or data analysis projects. 📊💻

## 💪 Why Use Realtime-Flipkart API?🌟
<ul>
	<li>Real-time product data access</li>
	<li>4x faster response times</li>
	<li>Comprehensive product details</li>
	<li>Regular category updates</li>
	<li>Multiple search options</li>
	<li>Reliable & stable endpoints</li>
</ul>

## 👥 Who Should Use the API?
<ul>
	<li>E-commerce businesses</li>
	<li>Price comparison services</li>
	<li>Market researchers</li>
	<li>Inventory management systems</li>
	<li>Dropshipping businesses</li>
	<li>Product analytics platforms</li>
</ul>

# Endpoint🎯
<p><code>GET /get-categories</code></p>
<ul>
	<li>Fetch top-level categories</li>
	<li>Weekly updated listings</li>
</ul>
<p><code>GET /get-subcategories</code></p>
<ul>
	<li>Access 2nd to 5th level categories</li>
	<li>Complete category hierarchy</li>
</ul>
<p><code>GET /product-details</code></p>
<ul>
	<li>Detailed product information</li>
	<li>Real-time pricing &amp; availability</li>
</ul>
<p><code>GET /products-by-category</code></p>
<ul>
	<li>Category-specific product lists</li>
	<li>Pagination support</li>
</ul>
<p><code>GET /products-by-brand</code></p>
<ul>
	<li>Brand-specific catalogs</li>
	<li>Filtered product listings</li>
</ul>
<p><code>GET /product-search</code></p>
<ul>
	<li>Product search functionality</li>
	<li>Multiple filter options</li>
</ul>

## Authentication 🔑
Authentication is handled through RapidAPI. Include your RapidAPI key in the request headers:

- x-rapidapi-host: real-time-flipkart-api.p.rapidapi.com
- x-rapidapi-key: your_rapid_api_key

## Example 💡: Get Subcategories 🌳
This endpoint allows you to retrieve subcategories for a given category ID on Flipkart.

### Request 🔍
<pre><code>GET https://real-time-flipkart-api.p.rapidapi.com/get-subcategories</code></pre>

### Parameters

|       Name         |Type                          |Description|
|----------------|-------------------------------|-----------------------------|
|    id      |      string                   |The category ID to fetch subcategories for (required)


### Example Request 💡
<pre>
<code>
curl --request GET \
	--url 'https://real-time-flipkart-api.p.rapidapi.com/get-subcategories?id=tyy' \
	--header 'x-rapidapi-host: real-time-flipkart-api.p.rapidapi.com'
	--header 'x-rapidapi-key: your_rapid_api_key'
</code>
</pre>

### Response 📊
The API returns a JSON object containing subcategories and their details:

### Parameters

|       Property         |Type                          |Description|
|----------------|-------------------------------|-----------------------------|
|    id      |      string                   |Unique identifier for the subcategory    
| title  |      string                   |Display name of the subcategory   
| url    |      string                  |URL to the subcategory page on Flipkart
| children    |      object                  |Nested object containing further subcategories

### Example Responce 💡

<pre>
<code>
{
  "subcategory_name": {
		"id": "string"
		"title": "string"
		"url": "string"
		"children": "dict"
	}

}
</code>
</pre>

## Example 💡

### base
```bash curl --request GET \
	--url 'https://real-time-flipkart-api.p.rapidapi.com/get-subcategories?id=tyy' \
	--header 'x-rapidapi-host: real-time-flipkart-api.p.rapidapi.com' \
	--header 'x-rapidapi-key: fd3f1114b1msh3d69719929fe501p1f1b72jsn2432d43bd3d1'
```

### Response
```
{
  "Power Bank Skins": {
    "id": "tyy/hwl",
    "title": "Power Bank Skins",
    "url": "https://flipkart.com/mobiles-accessories/power-bank-skins/pr?sid=tyy,hwl",
    "children": {}
  },
  "Mobiles": {
    "id": "tyy/4io",
    "title": "Mobiles",
    "url": "https://flipkart.com/mobiles-accessories/mobiles/pr?sid=tyy,4io",
    "children": {}
  },
  "Tablets": {
    "id": "tyy/hry",
    "title": "Tablets",
    "url": "https://flipkart.com/mobiles-accessories/tablets/pr?sid=tyy,hry",
    "children": {
      "Tablets with Call Facility": {
        "id": "tyy/hry/adj",
        "title": "Tablets with Call Facility",
        "url": "https://flipkart.com/tablets/tablets-with-call-facility/pr?sid=tyy,hry,adj",
        "children": {}
      },
      "Tablets without Call Facility": {
        "id": "tyy/hry/jut",
        "title": "Tablets without Call Facility",
        "url": "https://flipkart.com/tablets/tablets-without-call-facility/pr?sid=tyy,hry,jut",
        "children": {}
      }
    }
  },
}
```
## ℹ️ Important Notes
<ul>
<li>25-page listing limit</li>
<li>Use filters for maximum data</li>
<li>Check Tutorials for ID lookups</li>
</ul>

## Note
This API has been developed by a third-party, we are not affiliated with Flipkart.com in any way.

#### This endpoint provides a comprehensive view of Flipkart's category structure, allowing you to navigate through the product hierarchy and access specific category details. Use it to build category trees, create navigation menus, or analyze Flipkart's product organization! 🌟🛍️


## [Check Flipkart API](https://rapidapi.com/opendatapoint-opendatapoint-default/api/real-time-flipkart-api/playground)
