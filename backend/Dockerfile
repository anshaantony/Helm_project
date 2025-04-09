# Use official Python image
FROM python:3.10-slim

# Set working directory to backend
WORKDIR /app/backend

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . /app
COPY ./frontend/templates /app/templates
COPY ./frontend/static /app/static

# Set environment variables for Flask
ENV FLASK_APP=/app/backend/app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_ENV=development

# Expose port Flask runs on
EXPOSE 5000

# Run the Flask app
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]
