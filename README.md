# Thorin and Company
Simple Flask Web application based on the [Clean Blog v5.0.10](https://github.com/StartBootstrap/startbootstrap-clean-blog/tree/v5.0.10) Bootstrap theme by [StartBootstrap](http://startbootstrap.com/) and [Jinja2 templating engine](https://jinja.palletsprojects.com).


## Technologies
- Python v3.11.3
- Flask v2.2.3
- Jinja2 v3.1.2
- Bootstrap v4.5.3
- jQuery v3.5.1

## Deployment
The application is deployed on Heroku.

Live Demo: https://flask-app-thorin-and-company.herokuapp.com

#### Deployment process using Heroku CLI:
- Login to Heroku:
    ```$ heroku login```
- Create a Heroku app:
    For existing repositories, simply add the heroku remote (connect to remote).
    ```$ heroku create example-app (or create using UI heroku)```
- Connect Git remote to Heroku:
    * By Heroku git URL ( URL can be obtained from the app's settings page on the Heroku):
    ```$ git remote add heroku <heroku-git-url>```
    * By Heroku CLI and app name (full string can be obtained from the app's deploy page):
    ```$ heroku git:remote -a example-app```
- Create requirements file:
    ```$ pip freeze > requirements.txt```
- Add gunicorn server to requirements:
    ```$ echo "gunicorn" >> requirements.txt```
- Create a Heroku Procfile:
    * Run the flask app using built-in Flask development server (not recommended):
    _Requires app.run() code in the `app.py` script_
    ```$ echo "web: python app.py" > Procfile```
    * Run the flask app using using the Gunicorn WSGI server (recommended for production environments):
    ```$ echo "web: gunicorn app:app" > Procfile```
- Commit all changes: Add Heroku settings
- Deploy:
    ```$ git push heroku master``` (or connect to GitHub using UI).



## Credits
- Content: [The Lord of the Rings Wiki](https://lotr.fandom.com/)
- Theme: [StartBootstrap Clean Blog v5.0.10](https://github.com/StartBootstrap/startbootstrap-clean-blog/tree/v5.0.10)
- Code based on [Code Institute walkthrough Project](https://codeinstitute.net/)