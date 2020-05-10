# [firebase_phaser_CORS](https://github.com/zombietimes/firebase_phaser_CORS)
The solution to Cross-Origin Resource Sharing (CORS).  

## Overview
The following error occurred.  
'''
Access to image at 'https://firebasestorage.googleapis.com/v0/b/...' from origin 'https://prototypesampledevelopment.web.app' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource.
'''
- I developed a firebase application for the web by using Phaser.  
- There are some image files on the firebase storage.  
- When a phaser draws the image files, the error has occurred.  
- This article is about the solution to the error.  
  
## Description
### Phenomenon
Phaser can't draw the image files on the firebase storage.  
![firebase_phaser_CORS_0000](https://user-images.githubusercontent.com/50263232/81491417-6774a180-92c9-11ea-87fa-78fe78ba0f97.png)  
  
### Reason
The domain of the image files is https://firebasestorage.googleapis.com/.  
The domain of the application is https://prototypesampledevelopment.web.app.  
The CORS policy prohibits access between different domains.  
- [CORS : Cross-Origin Resource Sharing](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
  
### Mesures
It allows CORS by using gsutil tool.  
- [CORS solution ](https://firebase.google.com/docs/storage/web/download-files)
![firebase_phaser_CORS_0001](https://user-images.githubusercontent.com/50263232/81491424-78251780-92c9-11ea-9d3b-7b497dfb0872.png)  
![firebase_phaser_CORS_0002](https://user-images.githubusercontent.com/50263232/81491431-83784300-92c9-11ea-8283-1404dd5f34a8.png)  
![firebase_phaser_CORS_0003](https://user-images.githubusercontent.com/50263232/81491434-90953200-92c9-11ea-9ea7-fdb646f2f009.png)  
![firebase_phaser_CORS_0004](https://user-images.githubusercontent.com/50263232/81491440-9b4fc700-92c9-11ea-94ce-33d636866816.png)  
![firebase_phaser_CORS_0005](https://user-images.githubusercontent.com/50263232/81491445-a86cb600-92c9-11ea-91a9-46f34af8e522.png)  
  
## Relative link
- [firebase : web app platform](https://firebase.google.com/)
- [phaser : web game library](https://phaser.io/)
- [Google local server : Google chrome extentions](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb?hl=en)

## License
BSD 3-Clause, see `LICENSE` file for details.  

