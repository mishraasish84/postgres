#####################How to connect to DB through Support WEB START #####################

2️⃣ Access pgAdmin:

Open your browser and go to http://localhost:5050
Login with:
Email: admin@mylab.com
Password: adminpassword
3️⃣ Add a New Server in pgAdmin:

Click "Add New Server"

In the General tab:

Name: PostgreSQL (or anything you like)
In the Connection tab:

Host: postgres
Port: 5432
Username: admin
Password: admin
Click Save
###################How to connect to DB through Support WEB END ######################

#########################How to connect to DB Directly START #################

You can connect to the PostgreSQL database directly using the following methods:

1️⃣ Using psql from the Host Machine
If psql (PostgreSQL client) is installed on your host machine, you can connect using:

bash
Copy
Edit
psql -h localhost -U admin -d mydb
It will prompt for the password (admin as per your docker-compose.yml).

Alternatively, specify the password inline:

bash
Copy
Edit
PGPASSWORD=admin psql -h localhost -U admin -d mydb
2️⃣ Using psql Inside the Container
If psql is not installed on your host, you can connect directly inside the PostgreSQL container:

bash
Copy
Edit
docker exec -it postgres_container psql -U admin -d mydb
3️⃣ Using Any PostgreSQL Client (DBeaver, pgAdmin, etc.)
You can connect using DBeaver, HeidiSQL, or any SQL client using:

Host: localhost
Port: 5432
Username: admin
Password: admin
Database: mydb

#########################How to coonect to DB Directly END ###################
