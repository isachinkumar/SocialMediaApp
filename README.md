# Sociopedia-Social-Media-App
A full-stack social media web application that allows users to post, like, add friends and delete posts. A post is an image along with a description.

# Api Documentation :


### 1. **Register to Social-Media-App**

  ```http
  POST /auth/register
  ```
- Row body structure for a post request of file attchment :

  | Parameter      | Type               | Required  | Description              | Default |
  | :------------- | :----------------- | :-------- | :----------------------- | :------ |
  | `firstName`         | `string`           | **true**  | User First Name  | -       |
  | `lastName`         | `string`           | **true**  | User Last Name  | -       |
  | `email`         | `string`           | **true**  | User Email  | -       |
  | `password`         | `string`           | **true**  | User Password  | -       |
  | `picturePath`         | `string`           | **true**  | User Email  | " "       |
  | `friends`         | `array of strings`           | **false**  | User Password  | [ ]      |
   | `location`         | `string`           | **true**  | User Email  | -       |
  | `occupation`         | `string`           | **true**  | User Password  | -       |
 
- Example for post request through **Postman** [form-data] (using a local storage file)

  | Key     | value |
  | :------ | :------ |
  | firstName |    Ankita     |
  | lastName |    Gurwan     |
  | email |    ankitgur03@gmail.com     |
  | password |    password     |
  | picturePath |    https://res-console.cloudinary.com/dyufvjigd/thumbnails/v1/image/upload/v1689438573/cWFzZXRpcjA5d2k0c2t0cXdrc3U=/grid_landscape     |
  | location |    village khaira kalan     |
  | occupation |    student     |

- Example Response on success **(status code 201)**
  ```javascript
  {
    "firstName": "Ankita",
    "lastName": "Gurwan",
    "email": "ankitgur03@gmail.com",
    "password": "$2b$10$RWR3BZhK.EPphmQ1WZLPY.jmGV76YWMKqrgnDXUoTfTp/lO8vYGJC",
    "picturePath": "https://res-console.cloudinary.com/dyufvjigd/thumbnails/v1/image/upload/v1689438573/cWFzZXRpcjA5d2k0c2t0cXdrc3U=/grid_landscape",
    "friends": [],
    "location": "village khaira kalan",
    "occupation": "student",
    "viewedProfile": "459",
    "impressions": "393",
    "_id": "64b97b5654805eabeaf05f0c",
    "createdAt": "2023-07-20T18:22:14.146Z",
    "updatedAt": "2023-07-20T18:22:14.146Z",
    "__v": 0
    }
  ```

### 2. **Login to Social-Media-App**

  ```http
  POST /auth/register
  ```
- Row body structure for a post request of file attchment :

  | Parameter      | Type               | Required  | Description              | Default |
  | :------------- | :----------------- | :-------- | :----------------------- | :------ |
  | `email`         | `string`           | **true**  | User Email  | -       |
  | `password`         | `string`           | **true**  | User Password  | -       |

 
- Example for post request through **Postman** [form-data] (using a local storage file)

  | Key     | value |
  | :------ | :------ |
  | email |    ankitgur03@gmail.com     |
  | password |    password     |


- Example Response on success **(status code 201)**
  ```javascript
    {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0Yjk3YjU2NTQ4MDVlYWJlYWYwNWYwYyIsImlhdCI6MTY4OTg3NzQzNn0.EVXx83HzABLOGaf5UZ3AC0TQf_bYVWjR1foKgp580FI",
        "user": {
            "_id": "64b97b5654805eabeaf05f0c",
            "firstName": "Ankita",
            "lastName": "Gurwan",
            "email": "ankitgur03@gmail.com",
            "password": "$2b$10$RWR3BZhK.EPphmQ1WZLPY.jmGV76YWMKqrgnDXUoTfTp/lO8vYGJC",
            "picturePath": "https://res-console.cloudinary.com/dyufvjigd/thumbnails/v1/image/upload/v1689438573/cWFzZXRpcjA5d2k0c2t0cXdrc3U=/grid_landscape",
            "friends": [],
            "location": "village khaira kalan",
            "occupation": "student",
            "viewedProfile": "459",
            "impressions": "393",
            "createdAt": "2023-07-20T18:22:14.146Z",
            "updatedAt": "2023-07-20T18:22:14.146Z",
            "__v": 0
            }
    }   
  ```


