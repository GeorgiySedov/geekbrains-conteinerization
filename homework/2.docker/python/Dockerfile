FROM python:alpine3.16

WORKDIR app_py_less2
COPY . ./app
RUN pip install -r ./app/requirements.txt

EXPOSE 8080

ENTRYPOINT ["python3", "./app/app.py"]
