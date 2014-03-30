trust-based-reco
================

1. TO run the code
  
  Import google-play-services_lib from 
  
  .\adt-bundle-windows-x86_64-20131030\adt-bundle-windows-x86_64-20131030\sdk\extras\google\google_play_services
  
  Import G+ login into existing workspace
  
  Go to build path -> Android -> Library -> Add -> select google-play-services_lib
  
  
  
2. Setting mongodb in windows

        http://www.mkyong.com/mongodb/how-to-install-mongodb-on-windows/
        
        
3. Used Yelp API to get details of particular cuisine. Make necessary changes to consumer key and other details in file YelpApi2.java
        

To import CSV to mongodb

1. Store xls or csv in UTF8 text
2. mongoimport -d mydb -c things --type csv --file C:\Users\soganesa\Desktop\FarmersMarket8.txt --headerline
	If the above gives UTF8 character exception then there are some non convertable UTF8 characters
	
For Windows:

	1. Install iconv
		http://dbaportal.eu/2012/10/24/iconv-for-windows/
	2. iconv -f utf-8 -t utf-8 C:\Users\soganesa\Desktop\FarmersMarket.txt > FarmersMarket8.txt

	Then do mongoimport -d mydb -c things --type csv --file C:\Users\soganesa\Desktop\FarmersMarket8.txt --headerline
	
in Mondo shell

1. use mydb
2. db.things.find()
3. db.things.find()[3] to see one particular record.
