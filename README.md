# Jinja2 live parser based on sahilsk app

## Start Dev

### Clone + pip
```bash
# create a venv
git clone git@github.com:attiliogreco/jinja2-live-parser.git
pip install -r requirements.txt
python parser.py
```

### Dockerfile
```bash
docker build -t mydocker/j2parser .
```

## Usage

You are all set, go to `http://localhost:5000/` and have fun.  
You can add any custom filter you'd like in `filters.py`.  Just make sure the function's name starts with `filter_`.

Buildin filter get from Ansible filters

## Preview

[preview](https://jinja2.agreco.it/)

## Install with docker
```bash
docker run -d -p 8080:8080 attiliogreco96/jinja2-live-parser
```

## install uwsgi server in emperor mode.

```
[uwsgi]
plugin=python36
projectname = jinja2

#config
chdir = path-to-app
home = path-to-venv

wsgi-file = path-to-app/app.py
callable = app
vacuum = true

logto= /log-file/jinja2.log

# Worker handling
cheaper-algo=spare2
cheaper=1
cheaper-initial=2
processes=4
cheaper-step=1

# Stats
socket = /var/run/uwsgi/jinja2.sock
memory-report=true
stats=/run/uwsgi/stats/jinja2-live-parser.sock
```
