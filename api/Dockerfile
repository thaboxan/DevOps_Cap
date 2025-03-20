# Use Python 3.9
FROM python:3.9

# Set working directory in container
WORKDIR /usr/src/app

# Set PATH for pip
ENV PATH="/usr/local/bin:${PATH}"

# Upgrade pip
RUN pip install --upgrade pip

# Copy requirements first to leverage Docker cache
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application
COPY . .

# Expose port 8000
EXPOSE 80

# Command to run FastAPI application using uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
