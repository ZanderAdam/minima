FROM python:3.11-slim-buster

# Set the working directory
WORKDIR /app

# Copy the project files into the container
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir uv 
RUN uv pip install --no-cache-dir -r pyproject.toml --system

# Expose the port the server will run on
EXPOSE 8000

# Command to start the server
CMD ["uv", "run", "minima"]