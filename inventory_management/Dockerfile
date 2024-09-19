# Your Solution
# Use Python 3.10 slim image as base.
FROM python:3.10-slim 

# Set working directory to /app.
WORKDIR /app

# Copy requirements.txt into /app.
COPY requirements.txt .

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy app code into /app.
COPY . .

# Container listens on port 81.
EXPOSE 81

#  Run Uvicorn server with app on port 81.
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "81"]