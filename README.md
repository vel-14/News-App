# News-App

## Description
News Web Application using Flask and NewsAPI. The web page will display top headlines and a search bar where the user can enter a query, after processing the query, the webpage will display all relevant articles (up to a max of 100 headlines).

## API Key generation
In order to use the News API in our application, we need to generate a unique API key from https://newsapi.org/. In order to use the News API in our application, we need to generate a unique API key from https://newsapi.org/. 

## Creating backend endpoints
There are two things we want from our application :

* Display top headlines when the web application is opened.
* Show results based on a search query.

### Display top headlines
To get the top headlines we will use get_top_headlines function from newsapi library. We can pass parameters to this function like country, language, sources, etc. In this application, we will pass an additional parameter called page_size to get all the headlines. The newsapi library function only returns the top 20 articles but it also has a field called totalResults in the JSON response object. We will modify our function call to fetch all results using the page_size parameter.

### Show results based on a search query
This will be related to a post request We are going to use the get_everything function with parameters like query sources, domains, language, sorting based on, and page_size. We will fetch all sources with the help of the get_sources function of newsapi and to fetch all domains we will use ‘URL’ property of each source.
