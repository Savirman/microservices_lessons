FROM python:slim-buster
RUN pip install flask
ADD . /app
EXPOSE 8000
ENTRYPOINT python app/app.py runserver 0.0.0.0:8000

