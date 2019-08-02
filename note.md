## Firebase Cloud Messaging HTTP protocol

1. POST URL:  https://fcm.googleapis.com/fcm/send  

2. Add Headers Authorization: key=<legacy_server_key> OR Authorization: key=<server_key>   

3. Json context example:  
    * Send FCM to single device  :  
        > {  
        > "to" : "YOUR_FCM_TOKEN_WILL_BE_HERE",  
        > "collapse_key" : "type_a",  
        > "notification" : {  
        >     "body" : "Body of Your Notification",  
        >     "title": "Title of Your Notification"  
        > }  
        > }  

    * Send FCM to multiple device   
        > {  
        > "registration_ids": ["fcm_token1", "fcm_token2"] ,  
        > "collapse_key" : "type_a",  
        > "notification" : {  
        >     "body" : "Body of Your Notification",  
        >     "title": "Title of Your Notification"  
        > }  
        > }  





# Reference :
-官方文件: https://firebase.google.com/docs/reference/fcm/rest/v1/projects.messages  
-教學範例: https://medium.com/android-school/test-fcm-notification-with-postman-f91ba08aacc  
-Stackoverflow大神: https://stackoverflow.com/questions/45309674/fcm-with-postman-the-request-was-missing-an-authentication-key-fcm-token  
    
