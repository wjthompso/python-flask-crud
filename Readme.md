Here are the commands that were used.

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

To create the local database:
1. Activate the environment, if the environment isn't running.
`source env/bin/activate`
2. In the command line, open an interactive python3 shell:
`python3`
3. Then type the following and hit enter:
`from app import db`
4. Then, type the following and hit enter:
`db.create_all()`
5. The database is setup, go ahead and exit out of the interactive python shell using the following command.
`exit()`

A little code to add

