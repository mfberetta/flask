FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
RUN pip install flask_bootstrap
RUN pip install flask-wtf
RUN pip install flask_sqlalchemy
RUN pip install flask_login
RUN pip install email_validator
RUN pip install pymysql
EXPOSE 5000
COPY . .
CMD ["flask", "run"]