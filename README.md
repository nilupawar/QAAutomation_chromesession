NOTE: Details in this repo can be used for other webdriver ( firefox/Ghecko , edge etc ) as well

Read more about JSONWire protocol from https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol


Chromedriver session is started using 'chromedriver -p <port_number>' -> endpoint URL : http://localhost:9515 (default)
When ChromeDriver is started in Docker-machine(windows 10 Home edition) (default port exposed inside docker is 4444) end point URL : http://<Usually_IP_IS_192.168.99.100>:4444/wd/hub
```
	Get the ip address of docker-machine using command "docker-machine ip default"
```
	
Please refer postman collection to see how to form end-point request

### Start a Chrome session - 
```
		METHOD 	- Post
		URL 	- <EndPointURL>/session
		Body 	-  
				{
					"desiredCapabilities": {
						"caps": {
							"browserName": "chrome",
							"version": "",
							"platform": "ANY"
						}
					}
				}	
```

### Get status of the driver
```
		METHOD 	- GET
		URL 	- <EndPointURL>/status
		BODY	- N/A	 
```

### Get details of all the active sessions with driver
```
		METHOD	- GET
		URL 	- <EndPointURL>/sessions
		BODY	- N/A
```

### Get the window handle of all the opened browser instances
```
		METHOD	- GET
		URL	- <EndPointURL>/session/{{sessionId}}/window_handles
		BODY	- N/A
```

### Navigate to browser URL
```	
		METHOD	- POST		
		URL	- <EndPointURL>/session/{{sessionId}}/url
		BODY	-
			{
				"url":"http://www.google.com"	//Never forget to write http:// otherwise you will get invalid arguments error
			}
```

### Get current URL
```
		METHOD	- GET
		URL	- <EndPointURL>/session/{{sessionId}}/url
		BODY	- N/A
```

### Delete any browser session
```
		METHOD	- DELETE
		URL	- <EndPointURL>/session/{{sessionId}}
		BODY	- N/A
```

### Take screenshot
```
		METHOD	- GET
		URL	- <EndPointURL>/session/{{sessionId}}/screenshot
		BODY	- N/A
```

		
		

		
		
		
	
		
		
		
