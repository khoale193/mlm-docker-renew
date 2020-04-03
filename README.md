# docker-mlm
Docker for MLM project

## Available services
 - MLM Member (Angular)
 - MLM Admin (Angular)
 - MLM Backend (Golang)
 - MLM Resource (Anguar)
 - Webserver (Nginx)

## Prepare
1. Setting up the database by yourself, we do not use the database in docker because of un-safe reasons

2. Install Docker at https://docs.docker.com/install/linux/docker-ce/ubuntu/

3. Clone git mlm-ng-goapi (Golang) into folder ./backend/mlm-ng-goapi

4. Clone git mlm-ng (Angular) into folder ./member/mlm-ng

5. Clone git mlm-ng-admin (Angular) into folder ./admin/mlm-ng-admin

6. Clone git mlm-ng-admin (Angular) into folder ./resource/mlm-ng-admin

## Deploy services
1. Deploy webserver
```
docker-compose up -d webserver
```
2. Build backend-base docker images
```
cd backend \
&& docker build -t backend-base .
```
3. Deploy backend
```
docker-compose up -d backend
```
4. Deploy admin site
```
docker-compose up -d admin
```
5. Deploy member site
```
docker-compose up -d member
```

## Update services
Fetch and pull latest code, then run below command
```
docker-compose up -d --build member
```
