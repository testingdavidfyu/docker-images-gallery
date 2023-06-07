FROM python:3.9 

# path inside the image container
WORKDIR /app

EXPOSE 5050

COPY Pipfile Pipfile.lock ./

RUN pip install pipenv
RUN pipenv requirements > requirements.txt
RUN pip install -r requirements.txt

# copy all files from this directory into the image container's working directory
COPY . ./

CMD ["python", "main.py"]
