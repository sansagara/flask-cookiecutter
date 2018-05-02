FROM python:3.6.2

#Update the current pip install
CMD pip install --upgrade pip

# Copy all the requirements into the container
COPY requirements.txt ./

# Install all the dependencies needed to run the container
RUN pip install -r ./requirements.txt

# Copy the application and create the application folder in the container
COPY ./ /app/

# Set the working directory in the container
WORKDIR /app

# Run the application
CMD python manage.py runserver -h 0.0.0.0