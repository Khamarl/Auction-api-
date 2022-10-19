# Auction API overview 

The Auction API is built on REST principles, that can be used to access information about current auctions, bids and auction products. Users can interact with any of our URIs by using the specified HTTP request method.
<br>

## Getting Started 
<br>

### API Base URI 

All requests to our API are supposed to be sent to this endpoint. Below you will find a list of endpoints that the API supports.

    https://api.auction.com/api/v1/
<br>
    
### API endpoints: 

Auction information using the Auction API is simple. A standard API request is performed using the API's `auctions` endpoint:


| Endpoint            | Description                                                  | URI                                        |
| ------------------- | -------------------------------------------------------------|--------------------------------------------|
| /auctions           | This provides a list of auctions available                   |  `http://api.auction.com/auctions`         |
| /auctions/:id        | This will return an auction with corresponding id           |  `http://api.auction.com/auctions/:id`     |
| /auctions/random    | This will return a random auction based on its id            |  `http://api.auction.com/auctions/random`  |
| /auctions/search    | Text                                                         |  `http://api.auction.com/auctions/search`  |
| /auctions/upcoming  | This will return auctions upcoming in the next week          |  `http://api.auction.com/auctions/upcoming`|
| /auctions/:id/bids  | This will return the bids of a prticular auction with that id|  `http://api.auction.com/auctions/:id/bids`|

<br>

## About auction endpoints:

| Endpoint                 | Type                 |
| -------------------------| ---------------------|
| `GET`/auctions           |                      |  
| `GET`/auctions/:id       |                      |  
| `GET`/auctions/random    |                      |  
| `GET`/auctions/search    |                      |  
| `GET`/auctions/upcoming  |                      | 
| `GET`/auctions/:id/bids  |                      |  

As a RESTful application, we therefore use GET , PATCH, POST and DELETE HTTP requests to deal with our data. 

### Example request:

`get https://api.auction.com/auctions`


       results: [] 50 items
         0: {} 9 keys
         title: "Banged up Saxo"
         starting bid: "£5"
         current bid: "£5.01"
         remaining duration: "2 days"
         odomoter: "450,736"
         fuel type: "petrol"
         colour: "blue"
         keys: "no"
         transmission: "manual"

<br>

## Query URI's




## Status codes 

| Status code         | Description                                                  |
| ------------------- | -------------------------------------------------------------|
| 200                 | All checks complete                                          |
| 401                 | Unauthorized Missing or incorrect API token in header.       |
| 404                 | This page does not exist                                     |  
| 500                 | Internal Server Error                                        |  

