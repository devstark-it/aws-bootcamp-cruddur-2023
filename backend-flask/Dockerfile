FROM python:3.11.2-slim-buster

# Inside Container
# make new folder inside the Container 
WORKDIR /backend-flask

# Outside Container -> Inisde Container
# this contains the libraries we want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container
# Install the python libraries  used for the app
RUN pip3 install -r requirements.txt

#Outside Container -> Inside Container
# . means everything in the current directory 
# first period . - /blackend-flask(outside container)
# second period . - /blackend-flask(inside container)
COPY . .

# Set Environment Variables  (Env Vars)
# Inside Container and will remain set when container is running 
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"] 