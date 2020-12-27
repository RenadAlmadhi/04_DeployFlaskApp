FROM python:stretch
WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/requirements.txt
RUN pip install --upgrade pip && pip install --no-cache-dir -r /usr/src/app/requirements.txt

COPY main.py /usr/src/app/main.py

ENTRYPOINT ["gunicorn", "-b", ":8080", "main:APP"]

