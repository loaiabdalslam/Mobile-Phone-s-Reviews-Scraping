# Review Mobile Phone Using GSMRENA

we try to make a web service for scrapping phone's Reviews we will use BeautifulSoup as Scrapping Lib and will use GSMRENA.com 
to get our Data from .

### how to know what's a Right architecture for Structure ? 

. first you want to know how to Start making this web service , the first point we need to start checking our data provider yea i mean gsmrena and look closley at this website , and i observed it uses query string and that's what we are want exactly .. when you try using beautifulsoup the first point you want to know is you need query string that's Example of Query String :
https://www.gsmarena.com/res.php3?sSearch=apple
and that's part " ?sSearch=apple  " is a query string with a param sSearch equal apple ..

let's see website's Architecture and observe what is the best way to collect theese Next Point :
- Searching : https://www.gsmarena.com/res.php3?sSearch=apple then you can get id and Searching any mobile
- Reviews : https://www.gsmarena.com/oppo_f3-review-1608.php
- Mobile Details : https://www.gsmarena.com/oppo_f3-8669.php

Looking at Mobile Details Url what you obeserved right now .. yea this is a pattern at Query /brand_type_PhoneId.php
here our starting point


### Searching Function Arcitecture :
- Create Url Function For Passing url with it
- Create GetResults Function (Function's Architecture):
    - First open url using urlopen,url Function
    - Get name and img for Resulted Phones by BeautifulSoup find() and find_all()
    - For Each phone name Clean and replace then Get id by substring function or indexing
    - Return Data after Do that !
- Create DisplayResults by using HTML and images



## ShowReviews and Phone's Details

- Create getPhonebyID To get specific Phone based on its ID (We will use this Function Later )
- Create UrlPhone For Routing Theese Quires
- Create getPhoneDetails to Filter and Display phone's Details Easly 
- Create getPhoneReviews to Display Phone's Reviews


### Let's Make a Small Test about How we can Make a query string Search to get some data about specific Phone !
- Start Search by GetResults() and Try Displaying it getDisplayResults() Using To Client To Select What's Phone he need to know about it !
- Then Select specific Phone's id and Try to Check it inner getPhoneDetails() To Get phone's Details 
- Then Select specific Phone's id and Try to Check it inner getPhoneReviews() To Get phone's user reviews



