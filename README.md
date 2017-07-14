# CatalogApp - Udacity Project: Databases & Applications

The **Catalog Application Project** is the fourth project I have completed in the **Full Stack Web Developer Nanodegree** offered by **_Udacity_**.  This project simulates a backend database that feeds a frontend page for authenticated users to view, add, edit, and delete items in a catalog.

The files in this repository will setup the **_Vagrant VM_** needed to run this application on a local machine.

## Table of Contents

* Setup
* Usage
* Authors
* Acknowledgments

## Setup

1. Fork this repository to your GitHub account.

2. Clone the forked repository to a directory on your local machine.

3. From a terminal or command line interface, change directories into the **_vagrant_** folder.
```
cd CatalogApp; cd vagrant
```
4. Setup the **_Vagrant VM_**.
```
vagrant up
```
5. SSH into the **_Vagrant VM_**.
```
vagrant ssh
```
6. Follow the **_Vagrant VM_** prompts and change directories.
```
cd /vagrant
```
7. Change directories to the **_catalog_** folder.
```
cd catalog
```

## Usage

**_Running the application in the Vagrant VM_**

1. Run **_app.py_**.
```
python app.py
```
2. Open a web browser to visit the frontend
```
http://localhost:5000/catalog
```
3. You can also access the catalog data via the following JSON endpoints.
```
http://localhost:5000/catalog/JSON
```
```
http://localhost:5000/catalog/items/JSON
```
```
http://localhost:5000/catalog/<int:category_id>/items/JSON  # Where '<int:category_id>' is a number 1-8
```
```
http://localhost:5000/catalog/item/<int:item_id>/JSON  # Where '<int:item_id>' is a number for the item's key in the DB
```
```
http://localhost:5000/catalog/users/JSON
```

**_Deleting and rebuilding the database_**

1. Remove **_catalogapp.db_**

2. Run **_catalog_builder.py_**
```
python catalog_builder.py
```
3. Re-run **_app.py_**
```
python app.py
```

## Authors

* **Sean Magrann** - AT&T Services, Inc. | Emerging Technologies

## Acknowledgements

* [Udacity](https://www.udacity.com/) - Programming Foundations with Python
* [Udacity](https://www.udacity.com/) - The Backend: Databases & Applications
* [Google](https://developers.google.com/) - OAUTH User Authentication
* [Facebbok](https://developers.facebook.com/) - OAUTH User Authentication
