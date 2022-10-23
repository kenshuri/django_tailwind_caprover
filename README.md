# Minimal template for a Django project configured with TailwindCSS and daisyUI ready to be deployed to CapRover

This code will set-up a Django Project with tailwindCSS and daisyUI ready to be deployed to CapRover.

This repo also contains a github action to deploy the app when the main barnch is updated.

The details related to this repo are available on my [blog](https://blog.kenshuri.com/posts/006_from_heroku_to_capRover.md).

## Set-up the project

To set-up the project from scratch, run the following commands in your terminal.

```shell
git clone https://github.com/kenshuri/django_tailwind_caprover.git
cd django_tailwind_caprover
python -m virtualenv venv
venv/scripts/activate
pip install -r requirements.txt
cd jstoolchains
npm install
```

You're good to go my friend!

## Start your project 

To see your project in action, open 2 terminals.

In the first terminal run:
```shell
cd django_tailwind_caprover
cd jstoolchains
npm run tailwind-watch
```

In the second terminal run:
```shell
cd django_tailwind_caprover
python manage.py runserver
```

As prompted, open the page http://127.0.0.1:8000/ and enjoy 🚀

Note that changes in your html template `blogApp\templates\blogApp\index.html` automatically updates what you see in your browser.

## Deploy your project to CapRover

Steps for installing caprover are details in [this blog post](https://blog.kenshuri.com/posts/006_from_heroku_to_capRover.md)

#### Create a CapRover app

#### Deploy to CapRover

In the terminal run
```shell
caprover deploy
```

Follow the prompts and chose the app you just created

#### Modify your app environments variables

Add the following environment variables to your app:

* DJANGO_DEBUG=TRUE
* DJANGO_SECRET_KEY --> Create a secret key
* APP_ALLOWED_HOSTS --> Your app address