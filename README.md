# OncoKB Curation Platform

OncoKB Curation Platform is built with lots of great open source JS libraries. AngularJS is used as framework. Bower is used to manage denpendencies. Yeoman is used to initiate project and angular-generator is used to create angular directive/service/factory etc. 

We use Google Firebase Realtime Database to store all information curators generated.

## Install project
1. install node version v10.16.3
2. Install npm & & yarn & grunt-cli (globally) 
3. yarn install

## config.json setting
Create config.json file under /app/data and paste following json in it replace firebaseConfig with your firebase config
and replace  following values in json if your oncokb-core is running in different port then change the port


```
{
    "curationLink": "http://localhost:8080/legacy-api/",  // Your endpoints URL specifically designed for curation platform.  
    "apiLink": "http://localhost:8080/legacy-api/",   // Your endpoints URL.   
    "internalPrivateApiLink": "http://localhost:8080/api/private/",
    "privateApiLink": "http://localhost:8080/api/private/",   // Endpoints are specifically designed to use internally.
    "publicApiLink": "http://localhost:8080/api/v1/",
    "websocketApiLink": "localhost:8080/api/websocket/",
    "testing": false,   // If the testing is set to ture, all endpoints will be disabled and will use the files from web/yo/app/data folder.
    "production": false,    // If the production is set to ture, all endpoints will be enabled and reviewed data will be updated to MySQL database.
    
    // Click "Settings" button in Dev Oncokb Curation Firebase Console and choose project settings. Under General tab you will find Firebase SDK snippet section which has this config
    "firebaseConfig": {  
        "apiKey": "",
        "authDomain": "",
        "databaseURL": "",
        "projectId": "",
        "storageBucket": "",
        "messagingSenderId": "",
        "appId": ""
    }
}
```


## FAQs      
#### Can’t getAllUsers() because of the different rules set in Firebase. It still shows 'don’t have access...' after logging in successfully.         
   Add rules to the database.     

License
--------------------

OncoKB free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License, version 3, as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

A public instance of OncoKB (https://oncokb.org) is hosted and maintained by Memorial Sloan Kettering Cancer Center. It provides access to all curators in MSKCC knowledgebase team.

If you are interested in coordinating the development of new features, please contact contact@oncokb.org.
