FROM python:3.9

WORKDIR /app

EXPOSE 5050

COPY Pipfile.lock Pipfile ./

RUN pip install pipenv

RUN pipenv lock --requirements > requirements.txt
RUN pip install -r requirements.txt

COPY . ./

CMD ["python", "main.py"]