Chromedriver session is started using 'chromedriver -p <port_number>'

### Start a Chrome session - 
	_REST Request_ 
		Method -Post
		URL - http://127.0.0.1:<port_number>/session
		Body -  
				{
					"desiredCapabilities": {
						"caps": {
							"browserName": "chrome",
							"version": "",
							"platform": "ANY"
						}
					}
				}	

	_CURL Request_
		curl --location --request POST 'http://127.0.0.1:9515/session' \
		--header 'Content-Type: application/json' \
		--data-raw '{
			"desiredCapabilities": {
				"caps": {
					"browserName": "chrome",
					"version": "",
					"platform": "ANY"
				}
			}
		}'