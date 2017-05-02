# PostgreSQL (9.6.2) and PostGIS (2.3.2) installation on Ubuntu Xenial64

1. PostgreSQL installation
```
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt xenial-pgdg main" >> /etc/apt/sources.list'
wget --quiet -O - http://apt.postgresql.org/pub/repos/apt/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install postgresql-9.6
```
2. PostGIS installation
```
sudo apt-get install postgresql-9.6-postgis-2.3 postgresql-contrib-9.6
sudo apt-get install postgis
```
4.	Check commit log
git log

5.	Check status
git status

6.	Push changes
git push origin master
