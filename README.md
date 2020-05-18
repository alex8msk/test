# Foodangels Readme

# App:
## Main tools:
- Flutter (Channel master, v1.15.10-pre.4)
- Android toolchain - develop for Android devices (Android SDK version 28.0.3)
- Xcode - develop for iOS and macOS (Xcode 11.3.1)
- Android Studio (version 3.5)
- Development IDE: Android Studio

## Libraries:
- cupertino_icons: ^0.1.3
- async: ^2.4.0
- shared_preferences: ^0.5.6+1
- http: ^0.12.0+4
- provider: ^4.0.4
- google_maps_flutter: ^0.5.21+3 #Don't change
- location: ^2.4.0
- flutter_rating_bar: ^3.0.1+1
- transparent_image: ^1.0.0
- google_sign_in: ^4.1.4
- like_button: ^0.2.0
- geohash: ^0.2.1
- sqflite: ^1.2.1
- flutter_svg: ^0.17.1
- url_launcher: ^5.4.2
- geolocator: ^5.3.0
- intl: ^0.16.1
- flutter_paginator: ^0.0.6
- firebase_core: ^0.4.0+9
- toast: ^0.1.5
- flutter_slidable: "^0.5.4"
- http_interceptor: ^0.2.0
## Other
- Plus a few libraries were copied into the project and modified - clustering_google_maps, flutter_paginator, assorted_layout_widgets

# Notes 
- Default widgets are from flutter/material.dart package. So the app is in material style.
- For installation detail, see https://flutter.dev/docs/get-started/install

## Deployment:
- flutter build ios
- flutter build android
- Then it can be deployed like native apps

# Server
## Installation
Install
- PostgreSQL database
- PostGIS
- Python3
- virtualenv
- virtualenvwrapper
## Running 
After installing the virtualenv and virtualenvwrapper environment, execute the following command to create a virtual environment:
```bash
# Create a workspace
> mkvirtualenv foodangels
# Activate the workspace
> workon foodangels
# Change to the root directory of this project, Install dependencies
> pip install -r requirements.txt
```
Create the foodangels database.
Database connection configuration in project settings (core/settings/base.py)
Adding PostGIS extension to Postgres.
Use the following command to migrate the table:
```bash
> python manage.py makemigrations
> python manage.py migrate
```
Create a superuser account to access the Django admin:
```
> python manage.py createsuperuser
```
Create a Social Application for Google at http://127.0.0.1:8000/admin/socialaccount/socialapp, with the following properties:

	Provider: Google
	Name: Google (or something similar)
	Client ID: your application Client ID (obtained in the Developers Console at APIs & auth –> Credentials).
	Secret Key: your application Client Secret
	Key: not needed (leave blank).
	Select the corresponding site.
