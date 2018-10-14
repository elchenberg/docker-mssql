# Run Microsoft SQL Server (for Linux) and Adminer in Docker

_Start a temporary Microsoft SQL Server and manage it using Adminer. This is intended for Microsoft SQL Server training at school._

## System Requirements

_Tested with __Docker version 18.06.1-ce__ and __docker-compose version 1.17.1__._

### Software

* Docker 1.10.0+
* Docker Compose 1.6.0+

### Disk Space

* Microsoft SQL Server Image: 1.5 GB
* PHP/Adminer Image: 90 MB
* Nginx Image: 20 MB

### Idle Memory Usage

_"At least 2GB of RAM" according to <https://hub.docker.com/r/microsoft/mssql-server/>_

* Microsoft SQL Server Container: 740 MB
* PHP/Adminer Container: 21 MB
* Nginx Container: 3 MB

## Usage

Run `make start` and Docker Compose builds and starts everything for you. When it is done, open a browser and got to <localhost:8080>.

Run `make stop` and everything will be shutdown. All changes made on the database server will be lost, so you will have to save your SQL queries elsewhere if you want to keep them.

You may use other tools to connect to the SQL server (e.g. Visual Studio Code: <https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-develop-use-vscode?view=sql-server-2017>) but then you probably won't be able to use Adminer to view your tables. I guess that's because the SQL server doesn't allow simultaneous connections by default.

## Login

* __System__: MS SQL (beta)
* __Server__: localhost:1433
* __Username__: sa
* __Password__: Password1
* Database: (empty)

## Links

* Docker Hub Official Repository __nginx__: <https://hub.docker.com/_/nginx/>
* Docker Hub Official Repository __adminer__: <https://hub.docker.com/_/adminer/>
* Docker Hub Public Repository __microsoft/mssql-server__: <https://hub.docker.com/r/microsoft/mssql-server/>
* Quickstart: Run SQL Server container images with Docker: <https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-2017>
* Use Visual Studio Code to create and run Transact-SQL scripts for SQL Server: <https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-develop-use-vscode?view=sql-server-2017>