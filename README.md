1. Run the PrintSearchAPI using Spring Tools Suite as a maven project. The PrintSearchAPI program will
create the database named "printdrawingdatabase" and a table named "printdrawings".
2. Use the .sql file named "PrintDrawings.sql" to fill up the "printdrawings" table with the data.
3. Import the "Print Drawing API-ScottMichaelAnderson.postman_collection" into Postman to create the collection for interacting
with the PrintSearchAPI @RestController endpoints.


# PrintDrawingSearchAPI - README

## Step #01

1. Using Spring Tools Suite (or your preferred IDE), open PrintDrawingSearchAPI.

2. Run the PrintDrawingSearchAPI as a "Spring Boot App".

3. Use the Postman API Platform and import the following .json file into Postman.
- Print Drawing API-ScottMichaelAnderson.postman_collection.json





## Step #02

1. Register your user at `http://localhost:8080/register/user`.
2. Enter username, password, and role.

-   Note: the roles variable must be in the following format with no spaces:
    -   "USER,ADMIN"
    -   "ADMIN,USER"
    -   "USER"
    -   "ADMIN"

## Step #03

1. Login your user at `http://localhost:8080/login`
2. You will be authenticated and you will be authorized to access the endpoints accessible with your specified role.

### Note: For Users without the "ADMIN" role

-   Users without "ADMIN" role can access the following Endpoints
    -   CREATE NEW TASK --> `http://localhost:8080/api/task/create`
    -   UPDATE TASK BY ID --> `http://localhost:8080/api/task/update/{id}`
    -   GET ALL TASKS --> `http://localhost:8080/api/getalltasks?pageNo=0&pageSize=10`
    -   GET TASK BY ID --> `http://localhost:8080/api/task/{id}`
    -   DELETE TASK BY ID --> `http://localhost:8080/api/task/delete/{id}`

### Note: For Users with "ADMIN" role

-   Users with "ADMIN" role can access the following Endpoints
    -   WHICH USER IS LOGGED IN --> `http://localhost:8080/admin/activeuser`
    -   GET ALL USERS --> `http://localhost:8080/admin/getallusers`
    -   GET USER BY ID --> `http://localhost:8080/admin/user/{id}`
    -   DELETE USER BY ID --> `http://localhost:8080/admin/user/delete/{id}`
