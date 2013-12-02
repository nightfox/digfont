digfont
=======

A font search website


To Contribute

* Fork the repo
* First we gotta do virtualenv setup.

```sh
$ sudo easy_install virtualenv
```
* Inside the repo, install your virtual enviornment.

```sh
virtualenv venv
```
* Initialize and activate virtualenv.

```sh
$ cd venv
$ . bin/activate
```
* Install requirements. Before that you would be actually inside venv directory so cd .. out of it to the base of the project.

```sh
$ sudo pip install -r requirements.txt
```
* Start the webserver.

```sh
$ foreman start -f Procfile.dev
```

* Create mongodb index from mongo shell

```sh
$ db.font.ensureIndex({name: 1});
```

* Add new links to mongodb
```sh
$ python manage.py add_url_file urls.txt
```

* Sync all fonts in db
```sh
$ python manage.py sync
```
