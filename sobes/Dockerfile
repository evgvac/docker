FROM python:3.7-alpine
WORKDIR /app
COPY ./files .
RUN pip install -r requirements.txt
CMD [ "flask", "run", "--host=0.0.0.0"]
