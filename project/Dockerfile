#Use a Python base image in version 2.7
FROM python:3.8.10

# I am using a different verson as specified because
# Python 2.7 reached the end of its life on January 1st, 2020.
# Please upgrade your Python as Python 2.7 is no longer maintained.

# Copying th contents
COPY /techtrends /app
WORKDIR /app
#ADD . .

#Install packages defined in the requirements.txt file
RUN pip install -r requirements.txt

#Ensure that the database is initialized with the pre-defined posts in the init_db.py file
RUN python init_db.py

#Expose the application port 3111
EXPOSE 3111

#The application should execute at the container start
CMD ["python", "app.py"]
