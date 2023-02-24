# Use an official Python runtime as a parent image
FROM python:3.9-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file into the container at /app
COPY requirements.txt /app

# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt


# Copy the rest of the application code into the container at /app
COPY . /app

# Set environment variables
ENV DJANGO_SETTINGS_MODULE=Online_Shop.settings
ENV PYTHONUNBUFFERED=1

# Expose the port that the Django app will run on
EXPOSE 8000

# Run the command to start the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
