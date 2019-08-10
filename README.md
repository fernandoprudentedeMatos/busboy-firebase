# busboy-firebase

## Using:

### Install:

`npm i busboy-firebase -s`

### Code Example:

	
~~~~

import * as functions from 'firebase-functions'
import * as admin from 'firebase-admin'
import * as express from 'express'
import fileUploadMiddleware from './middlewares/fileupload.middleware'

admin.initializeApp({
  ...
  });

...

const app = express();

app.post('/uploadfile', bfmiddleware, (req: any, res: any) => {
   // req.files[0]     <- here all files
   const fileOne = req.files[0];      
   const fileOne = req.files[0];   
    ...
              // req.files[0] Fields:
              //fieldname,
              //originalname: filename,
              //encoding,
              //mimetype,
              //buffer,
              //size,
   
})


export const api = functions.https.onRequest(app)

//Endpoint: http://localhost:<<port>>/<<appid>>/<<local firebase deploy>>/api/uploadfile
	
~~~~

### How post data:

1. method: post
2. header: Content-Type  multipart/form-data
3. Body (form-data)  with files


