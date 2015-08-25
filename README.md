# Creating demo data

To create demo data in your MongoDB execute generateData.js 

node generateData.js

# Run server

To run server execute:

node bin/www 


# Tools used

[httpie] - cmd line http client
install it 
sudo apt-get install httpie

Open two terminal
in first run server
in second run the commands in #make requests


# Make Requests

Creating and refreshing access tokens:

http POST http://localhost:8085/api/oauth/token grant_type=password client_id=android client_secret=SomeRandomCharsAndNumbers username=myapi password=abc1234
http POST http://localhost:8085/api/oauth/token grant_type=refresh_token client_id=android client_secret=SomeRandomCharsAndNumbers refresh_token=[Your refresh TOKEN]
```

Creating your article data:

http POST http://localhost:8085/api/articles title=NewArticle author='Saini Sarkar' description='Welcome to oauth' images:='[{"kind":"thumbnail", "url":"http://articlewritingservicesbyqlm.com/wp-content/uploads/2013/01/pen-write.jpg"}, {"kind":"detail", "url":"http://articlewritingservicesbyqlm.com/wp-content/uploads/2013/01/pen-write.jpg"}]' Authorization:'Bearer PUT_YOUR_Access_TOKEN_HERE'


Updating your article data:

http PUT http://localhost:8085/api/articles/YOUR_ARTICLE_ID_HERE title=NewArticleUpdated author='Saini Sarkar' description='Welcome to oauth' images:='[{"kind":"thumbnail", "url":"http://articlewritingservicesbyqlm.com/wp-content/uploads/2013/01/pen-write.jpg"}, {"kind":"detail", "url":"http://articlewritingservicesbyqlm.com/wp-content/uploads/2013/01/pen-write.jpg"}]' Authorization:'Bearer PUT_YOUR_Access_TOKEN_HERE'


Getting your data 

http http://localhost:8085/api/users/info Authorization:'Bearer PUT_YOUR_TOKEN_HERE'
http http://localhost:8085/api/articles Authorization:'Bearer PUT_YOUR_TOKEN_HERE'


