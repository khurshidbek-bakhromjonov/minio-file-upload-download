**File Upload**

Uploads a file to the Minio server.

Endpoint: `POST /app-minio/upload`

Request

- Method: `POST`

- Path: `/app-minio/upload`

- Content-Type: `multipart/form-data` 

- Parameters: `file` The file to be uploaded.

Response

- HTTP Status Code: `200 OK` - The file was uploaded successfully.
- HTTP Status Code: `500 Internal Server Error` - Failed to upload the file.


**File Download**

Downloads a file from the Minio server.

Endpoint: `GET /app-minio/download/{fileName}`

Request

- Method: `GET`
- Path: `/app-minio/download/{fileName}`
- Path Parameters: `fileName` The name of the file to be downloaded.

Response

- HTTP Status Code: `200 OK` - The file was found and returned as a downloadable attachment.
- HTTP Status Code: `500 Internal Server Error` - Failed to retrieve the file.


**Temporary URL Generation**

Generates a temporary URL for a file stored in the Minio server.

Endpoint: `GET /app-minio/temporary-url/{fileName}`

Request
- Method: `GET`
- Path: `/app-minio/temporary-url/{fileName}`
- Path Parameters: `fileName` The name of the file for which a temporary URL is to be generated.

Response
- HTTP Status Code: 200 OK - A temporary URL for the file was generated successfully.
- HTTP Status Code: 500 Internal Server Error - Failed to generate a temporary URL for the file.
