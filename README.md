# yt-de101-running-postgres-locally-with-docker

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
- shutting down docker: ```docker compose down```

## Module 2: Insert data into PostgreSQL using Python

- Install Python Libraries, copy requirements.txt from this GitHub repository
- Open your terminal, type pip ```install -r requirements.txt``` or ```pip3 install -r requirements.txt```, and press enter.
- In your terminal open jupyter notebook ```jupyter notebook```
- Execution ```de101-etl.ipynb```


