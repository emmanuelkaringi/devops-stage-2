# backend/Dockerfile

FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Copy the poetry.lock and pyproject.toml files
COPY pyproject.toml poetry.lock ./

# Install Poetry
RUN pip install poetry

# Install dependencies
RUN poetry config virtualenvs.create false && poetry install --no-dev

# Set PYTHONPATH
ENV PYTHONPATH=/app

# Copy the rest of the application
COPY . .

# Expose the port the app runs on
EXPOSE 8000

# Initialize the database
COPY ./app/initial_data.py .

# Run the initialization script and then the application
CMD ["sh", "-c", "python ./app/initial_data.py && uvicorn app.main:app --host 0.0.0.0 --port 8000"]