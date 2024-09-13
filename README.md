# Real-time Flipkart API 🛒🚀
The Real-time Flipkart API provides access to Flipkart's product category structure and metadata in real-time. This powerful tool allows developers to integrate Flipkart's extensive product catalog into their applications, websites, or data analysis projects. 📊💻

# Endpoint: Get Subcategories 🌳
This endpoint allows you to retrieve subcategories for a given category ID on Flipkart.

# Request 🔍
GET https://real-time-flipkart-api.p.rapidapi.com/get-subcategories

## Parameters

|       Name         |Type                          |Description|
|----------------|-------------------------------|-----------------------------|
|    id      |      string                   |The category ID to fetch subcategories for (required)


## Headers
- x-rapidapi-host: real-time-flipkart-api.p.rapidapi.com
- x-rapidapi-key: YOUR_RAPIDAPI_KEY

# Response 📊
The API returns a JSON object containing subcategories and their details:
## Parameters

|       Property         |Type                          |Description|
|----------------|-------------------------------|-----------------------------|
|    id      |      string                   |Unique identifier for the subcategory    
| title  |      string                   |Display name of the subcategory   
| url    |      string                  |URL to the subcategory page on Flipkart
| children    |      object                  |Nested object containing further subcategories

# Example 💡

### base
```bash curl --request GET \
	--url 'https://real-time-flipkart-api.p.rapidapi.com/get-subcategories?id=tyy' \
	--header 'x-rapidapi-host: real-time-flipkart-api.p.rapidapi.com' \
	--header 'x-rapidapi-key: fd3f1114b1msh3d69719929fe501p1f1b72jsn2432d43bd3d1'
```

 # Response

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


### This endpoint provides a comprehensive view of Flipkart's category structure, allowing you to navigate through the product hierarchy and access specific category details. Use it to build category trees, create navigation menus, or analyze Flipkart's product organization! 🌟🛍️


# [Check Flipkart API](https://rapidapi.com/opendatapoint-opendatapoint-default/api/real-time-flipkart-api/playground)
