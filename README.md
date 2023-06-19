# [Flask Argon Dash 2 PRO](https://appseed.us/product/argon-dashboard2-pro/flask/)

**Flask** starter styled with **[Argon Dashboard PRO](https://appseed.us/product/argon-dashboard2-pro/flask/)**, a premium `Bootstrap 5` KIT from [Creative-Tim](https://www.creative-tim.com?AFFILIATE=128200).
The product is designed to deliver the best possible user experience with highly customizable feature-rich pages. 

- 👉 [Flask Argon 2 PRO](https://appseed.us/product/argon-dashboard2-pro/flask/) - Product page
- 👉 [Flask Argon2 PRO](https://flask-argon-dash2-pro.onrender.com/) - `LIVE Demo` on Render

<br />

> Features

- ✅ `Up-to-date dependencies`
- ✅ UI Kit: [Argon Dashboard 2](https://www.creative-tim.com/product/argon-dashboard-pro?AFFILIATE=128200) (BS5 Version) by `Creative-Tim`
- ✅ `Database`: `SQLite`, MySql
  - Silent fallback to `SQLite`
- ✅ `DB Tools`: SQLAlchemy ORM, `Flask-Migrate`
- ✅ `Authentication`, Session Based, `OAuth` via **Github**
- ✅ Docker, `Flask-Minify` (page compression)
- 🚀 `Deployment` 
  - `CI/CD` flow via `Render`

![Argon Dashboard 2 PRO - Charts Page (Premium Bootstrap 5 Design)](https://user-images.githubusercontent.com/51070104/211157993-fd439b20-6117-4e02-b98c-9123866660e2.jpg)

<br />

## Start in `Docker`

> 👉 **Step 1** - Download & Unzip the code (`requires a purchase` from the official [product](https://appseed.us/product/material-dashboard2-pro/flask/) page)

```bash
$ unzip flask-material-dashboard2-pro.zip
$ cd flask-material-dashboard2-pro
```

<br />

> 👉 **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## Manual Build

> 👉 **Step 1** - Download & Unzip the code (`requires a purchase` from the official [product](https://appseed.us/product/material-dashboard2-pro/flask/) page)

```bash
$ unzip flask-material-dashboard2-pro.zip
$ cd flask-material-dashboard2-pro
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

Edit `.env` using `env.sample` or simply export the variables in the `environment`. Here are the expected values: 

- `DEBUG`: controls the `Development`, `Production` mode
  - Default `False` (production)
- `SECRET_KEY`: optional, random value used if not provided
- `DB credentials`
  - `Note`: if NOT provided, or wrong values, **SQLite is used**
  - `DB_ENGINE`, `DB_HOST`, `DB_NAME` ...
 
<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

## ✨ Code-base structure

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- routes.py                 # Define app routes
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- routes.py                 # Define authentication routes  
   |    |    |-- models.py                 # Defines models  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |    |    |-- includes/                 # HTML chunks and components
   |    |    |    |-- navigation.html      # Top menu component
   |    |    |    |-- sidebar.html         # Sidebar component
   |    |    |    |-- footer.html          # App Footer
   |    |    |    |-- scripts.html         # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- Dockerfile                           # Deployment
   |-- docker-compose.yml                   # Deployment
   |-- gunicorn-cfg.py                      # Deployment   
   |-- nginx                                # Deployment
   |    |-- appseed-app.conf                # Deployment 
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />

---
[Flask Argon Dash 2 PRO](https://appseed.us/product/argon-dashboard2-pro/flask/) - Provided by **[AppSeed](https://appseed.us/app-generator)**.
