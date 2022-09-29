# 316project
Open project for CS316: Database Systems

Github link: https://github.com/ChrstphrHll/316project

Group Name: Weak Entity Set

Contributors:
Christopher Hall 
Kegan Lovell
Molly Borowiak
Adam Kosinski
Aryan Mathur


# CS 316 Flask Application Example

### Starting the App
1. Run `conda create --name cs316 python=3.9.7`
2. Run `conda activate cs316`
3. Run `pip install -r requirements.txt`
4. Run `export FLASK_APP=flask_template.py` if on Mac
   Run `C:\path\to\app>set FLASK_APP=flask_template.py`
5. Run `flask run`
4. Run `python seed_test_db.py`


For deployment
`gunicorn -D -b 0.0.0.0 flask_template:app`
