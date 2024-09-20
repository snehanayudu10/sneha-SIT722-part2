# Use the official Python image from the Docker Hub
FROM python:3.11-alpine

# Set the working directory inside the container
WORKDIR /app/

# Copy the requirements file to the working directory
COPY book_catalog/requirements.txt /app/

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code to the working directory
COPY book_catalog/ /app/

# Specify the command to run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port","8000"]