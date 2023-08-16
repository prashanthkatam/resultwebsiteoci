# Dockerfile

FROM httpd

COPY . /usr/local/apache2/htdocs/

EXPOSE 8080 8081 80 443 22 8084 3306

# Dockerfile

FROM php:apache

COPY . /var/www/html

EXPOSE 80

RUN docker-php-ext-install mysqli

# References

https://stackoverflow.com/questions/666811/how-to-solve-fatal-error-class-mysqli-not-found

docker exec -it 8bcb80759a88 /bin/bash

#docker-php-ext-install mysqli

# Git Commands

git --version

git init

git add examwebsite/

git commit -m "first commit"

git remote set-url origin https://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@github.com/prashanthkatam/resultwebsiteoci.git

git push origin master

#apachectl restart (not required)

# Database Data Creation

create database customers;

use customers;

create table students(hallticketno varchar(255) NOT NULL, name varchar(255) NOT NULL, telugu varchar(255) NOT NULL, hindi varchar(255) NOT NULL, english varchar(255) NOT NULL, maths varchar(255) NOT NULL, science varchar(255) NOT NULL, social varchar(255) NOT NULL, totalmarks varchar(255) NOT NULL);

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS01', 'kiran', '99', '99', '99', '99', '99', '99', '554');
insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS02', 'Mahesh', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS03', 'Suresh', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS04', 'Srinivas', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS05', 'Naresh', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS06', 'Srikanth', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS07', 'Prashanth', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS08', 'Devansh', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS09', 'Shivansh', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS10', 'Sunny', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS11', 'Srinath', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS12', 'Shiva', '99', '99', '99', '99', '99', '99', '554');

insert into students (hallticketno, name, telugu, hindi, english, maths, science, social, totalmarks) values ('2022TS13', 'Boomaiah', '99', '99', '99', '99', '99', '99', '554');

# Push to Dockerhub

docker tag examwebsite:latest thebug2227/prodrepo:examwebsite

docker push thebug2227/prodrepo:examwebsite

thebug2227 is account name

prodrepo is dockerhub repo name

examwebsite is folder tagged to latest tag and pushed to thebug2227/prodrepo:examwebsite

First step is to tag a folder/file to tag name

Next step is to push it to the dockerhub
