FROM python:3.9-alpine
WORKDIR /app
ENV FLASK_APP=hello.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers

COPY requirements.txt /app/requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
COPY hello.py /app/hello.py
CMD [ "flask", "run"]