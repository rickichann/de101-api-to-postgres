# yt-de101

Data Architecture: 

![de101yt](https://github.com/rickichann/yt-de101-running-postgres-locally-with-docker/assets/53082147/1b00a7e5-d815-468b-a0a4-1a25501a7277)




🚀 **Ongoing Project!**

## Module 1: Running Postgres Locally with Docker
- Download and install:
  - [Docker](https://www.docker.com/products/docker-desktop/)
  - [TablePlus](https://tableplus.com/)
  - [Visual Studio Code](https://code.visualstudio.com/)
- Copy the `docker-compose.yaml` script from this GitHub repository.
- Open your terminal, type `docker-compose up -d`, and press enter.
- Open TablePlus, click on the "+" sign for a new connection, and choose PostgreSQL.
- Database Configuration
```
  - host: localhost
  - port: 5432
  - user: root
  - password: root123
  - database: devel
```
- Run the query below:

```
CREATE TABLE customer_data (
    unique_code VARCHAR(255) PRIMARY KEY,
    first_name VARCHAR(255),
    last_name VARCHAR(255),
    gender VARCHAR(10),
    email VARCHAR(255),
    username VARCHAR(255),
    dob TIMESTAMP,
    registered_date TIMESTAMP,
    phone VARCHAR(20),
    picture VARCHAR(255),
    post_code VARCHAR(10),
    address VARCHAR(255)
);
```
- shutting down docker: ```docker-compose down```

## Module 2: Insert data into PostgreSQL using Python

- Install Python Libraries, copy requirements.txt from this GitHub repository
- Open your terminal, type pip ```pip install -r requirements.txt``` or ```pip3 install -r requirements.txt```, and press enter.
- In your terminal open jupyter notebook ```jupyter notebook```
- Execution ```de101-etl.ipynb```

## Module 3: Seamless Data Transfer: PostgreSQL to Google Sheets Using Python
- Install gspread library, ```pip install gspread``` or ```pip3 install gspread```
- Extract data from postgreSQL using below query:
```
SELECT
      unique_code,
      concat(first_name,' ',last_name) full_name,
      phone,
      email,
      CAST(DATE_PART('year', AGE(dob)) AS INT) AS age
FROM
      customer_data
WHERE
      registered_date >= '2015-01-01 00:00:00'; 
```
- Create a blank spreadsheet : https://docs.google.com/spreadsheets/u/0/ and schema (unique_code, full_name, phone, email and age)
- Enable Google Cloud API
  - Go to the Google Cloud Console https://console.cloud.google.com/?hl=id
  - Click on the "Navigation menu" (three lines) and select "APIs & Services" > "Library".
  - Search for "Google Sheets API" in the search bar.
  - Click on "Google Sheets API" from the search results.
  - Click on the "Enable" button to enable the API.
  - Add email in gsheets,
  - In service accounts click email >> keys >> add key >> create new key >> json >> create

- Run python code !



