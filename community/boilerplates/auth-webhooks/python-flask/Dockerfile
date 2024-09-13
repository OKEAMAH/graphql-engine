FROM python:3.13.0a1-alpine

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

WORKDIR app
COPY auth-webhook.py auth-webhook.py

CMD ["gunicorn", "-b", "0.0.0.0:5000", "auth-webhook:app"]
