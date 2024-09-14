# Use a specific Python version for better reproducibility
FROM python:3.9

# Set the working directory in the container
WORKDIR /app

# Copy the dependency list and install dependencies
COPY requirements.txt ./
RUN pip install -r requirements.txt

# Copy the rest of the application code
COPY . .

# Run database migrations
RUN python manage.py migrate

# Expose the port that Django runs on
EXPOSE 8000

# Define the default command to run the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]



