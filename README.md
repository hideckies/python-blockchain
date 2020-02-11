# Implementation of blockchain with Python(Flask)

<br />

## 1. Set up `FLASK_APP` variable


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

<br /><br />

## 2. Start node server

Start a blockchain node server:<br />

```
flask run --port 8000
```

<br /><br />

## 3. Run application

Open a different terminal then start application as follows:<br />

```
python run_app.py
```

<br />

Check `http://localhost:5000`

<br /><br />

## 4. Multiple node

Start other nodes:<br />

```
flask run --port 8000 &

flask run --port 8001 &

flask run --port 8002 &

...

```

<br />

Connect a new node to the existing node in `register_with` endpoint<br />

```
curl -X POST http://localhost:8001/register_with -H "Content-Type: application/json" -d "{\"node_address\": \"http://localhost:8000\"}"

curl -X POST http://localhost:8002/register_with -H "Content-Type: application/json" -d "{\"node_address\": \"http://localhost:8000\"}"

...

```