[![Open in Visual Studio Code](https://img.shields.io/static/v1?logo=visualstudiocode&label=&message=Open%20in%20Visual%20Studio%20Code&labelColor=2c2c32&color=007acc&logoColor=007acc)](https://open.vscode.dev/microsoft/Web-Dev-For-Beginners)

Install docker and Dockerfile.mydb and run: 

```
docker build -t mysql -f Dockerfile.mydb . 
```
Install docker and Dockerfile.apache and run: 

```
docker build -t project_CongNghePhanMem -f Dockerfile.apache .
```
The next step is to run the following two commands:

```
1. docker run -d --name db -e MYSQL_ROOT_PASSWORD=mysql12345 -e MYSQL_USER=trannguyenhan -e MYSQL_PASSWORD=mysql12345 -e MYSQL_DATABASE=selling_computer -p 9906:3306 -d ngotanloi/mysql:latest

2. docker run -d --name selling-computer --link db -p 8000:80 -e DB_HOST=db -e DB_PORT=3306 -e DB_NAME=selling_computer -e DB_USERNAME=trannguyenhan -e DB_PASSWORD=mysql12345 ngotanloi/selling-computer
```
Access to `localhost:8000:80`, if have other process run in this port, you need stop this process.
