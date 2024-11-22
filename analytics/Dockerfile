# Use an official slim Python image as the base
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Copy all application files into the container
COPY . .

# Update system and install dependencies
RUN apt update -y && apt install -y build-essential libpq-dev

# Install Python dependencies
RUN pip install --upgrade pip setuptools wheel && pip install -r requirements.txt

# Expose the port the application listens on
EXPOSE 5153

# Command to run the application
CMD ["python", "app.py"]
