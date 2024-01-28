# yt-de101-api-to-postgres

🚀 **Ongoing Project!**

## Section 1: Download and Install
- [Docker](https://www.docker.com/products/docker-desktop/)
- [TablePlus](https://tableplus.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Python](https://www.python.org/downloads/)

## Section 2: Setup
- Copy the `docker-compose.yaml` script from this GitHub repository.
- Open your terminal, type `docker-compose up -d`, and press enter.
- Open TablePlus, click on the "+" sign for a new connection, and choose PostgreSQL.
- pip3 install -r requirements.txt 

## Section 3: Create Table in PostgreSQL

`CREATE TABLE customer_data (
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
);`

## Section 4: 



![image](https://github.com/rickichann/yt-de101-api-to-postgres/assets/53082147/5b84c480-17d5-41f2-a644-22575b1a3493)
