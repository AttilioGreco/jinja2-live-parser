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
