# Here are the command line arguments that were used.
Here's the original tutorial:
https://www.youtube.com/watch?v=Z1RJmh_OqeA


First, we had to create our virtual environment, so we have to install
`pip3 install virtualenv`
`virtualenv env` "env" is the name of the environment, which is the convention, but any name can be used.

Then we had to activate our virtual environment. When active, the "(env)" can be seen next to the command line prompt. We do this so that we can work with other people. We want to make sure all of the requirements are the same for everybody.
`source env/bin/activate`

Within that environment, install the necessary requirements.
`pip3 install flask flask-sqlalchemy`

After writing the .py file, various .html files, and .css file use the following command to run the local webserver. You can type `localhost:5000` to see the webpage
`python3 app.py`

# To create the local database:

1. Activate the environment, if the environment isn't running.
`source env/bin/activate`
2. In the command line, open an interactive python3 shell:
`python3`
3. Then type the following and hit enter:
`from app import db`
4. Then, type the following and hit enter:
`db.create_all()`
5. The database is setup and should show up as `test.db`, where the name seems to come from line 8 of the .py file: `app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///test.db'`, go ahead and exit out of the interactive python shell using the following command.
`exit()`

# Create the Procfile
In the repo, create the Procfile using touch.
`touch Procfile`
Then, open the Procfile using VSCode or another code editor and enter the following:
`web: gunicorn app:app` (I'm assuming the name of your python file is what you put after the semicolon)

# Pushing to Heroku
Type `heroku login` in your command line

Freeze requirements:
`pip3 install gunicorn`

`pip3 freeze > requirements.txt` (Check to make sure you're only putting the necessary requirements...)

`git init`
`git add .`
`git commit -m "enter your message here"`
`heroku create name-of-app`
`git remote -v` (This will show you where you're pushing your code to in heroku)
`git push heroku master`



