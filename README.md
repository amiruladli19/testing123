## Box Installation:
1.	vagrant box add gios gios.box
2.	vagrant init
3.	edit vagrant file
4.	vagrant up
5.	vagrant ssh

## Install geonode instance with:
1.	cd /vagrant
2.	git clone geonode (in geonode github 2.5.x)
3.	sudo pip install -e geonode
4.	copy local_settings.py dalam geonode/geonode
5.	cd geonode
6.	sudo paver setup
7.	cd
8.	cd vagrant

## Setup and run iFOSMap:
1.	Git clone iFOSMap(dalam github) --master

## Setup PostGIS
```
sudo su postgres 
```
1.	createuser -P ifos
2.	createdb -E 'utf-8' –l en_US.utf8 -O ifos -T template0 ifos
3.	createdb -E 'utf-8' -l en_US.utf8 -O ifos -T template0 ifos-spatial
4.	psql -f /usr/share/postgresql/9.3/contrib/postgis-2.1/postgis.sql ifos-spatial
5.	 psql -f /usr/share/postgresql/9.3/contrib/postgis-2.1/spatial_ref_sys.sql ifos-spatial
6.	 psql -d ifos-spatial -c 'GRANT ALL ON geometry_columns TO PUBLIC;'
7.	 psql -d ifos-spatial -c 'GRANT ALL ON spatial_ref_sys TO PUBLIC;'
8.	exit
9.	 sudo nano /etc/postgresql/9.3/main/pg_hba.conf <br/>
a.	# Change the ‘local all all’ from ‘peer’ to ‘trust’ <br/>
b.	Last line tambah <br/>
host all all all password <br/>
c.	# Save and exit nano <br/>
10.	  sudo nano /etc/postgresql/9.3/main/postgresql.conf
11.	  sudo service postgresql restart
12.	 sudo python manage.py makemigrations
13.	 sudo python manage.py migrate
14.	 sudo python manage.py syncdb
15.	python manage.py collectstatic
16.	 python manage.py createsuperuser
17.	python manage.py runserver 0.0.0.0:8000

## Git 

1.	git checkout –b develop origin/develop
2.	git checkout –b <some feature cth: module_name> develop
3.	git status
4.	git pull origin develop
5.	git add –all -- for all file in folder
6.	git add <file name> --for single file
7.	git add <folder name>/\*.py – for certain format only
8.	git commit –am “some message”
9.	git pull origin develop
10.	git checkout develop
11.	git merge din
12.	git push
```sh
sudo pip install django-nyt
sudo pip install django-material
sudo pip install django-sekizai
sudo pip install sorl-thumbnail
sudo pip install markdown
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

## PHP JSON
```
sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
      sudo apt-get install php5-sqlite
```

