# Implementation of blockchain with Python(Flask)

## 1. Set up `FLASK_APP` variable

<br />

First of all, set up the `FLASK_APP` environment variable.<br />
See [https://flask.palletsprojects.com/en/1.1.x/cli/](https://flask.palletsprojects.com/en/1.1.x/cli/) for details.<br /><br />


 for Mac, Linux:<br />

```
export FLASK_APP=blockchain.py 
```

<br />

for Windows CMD:<br />

```
set FLASK_APP=blockchain.py
```

<br />

for Windows PowerShell:<br />

```
$env:FLASK_APP=blockchain.py
```

<br />

## 2. Start node server

Start a blockchain node server:<br />

```
flask run --port 8000
```

<br />

## 3. Run application

Open a different terminal then start application as follows:<br />

```
python run_app.py
```

<br />

Check `http://localhost:5000`