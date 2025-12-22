# STEP 1 BUILD IMAGE -> docker build -t python-machine-learning .
# STEP 2 RUNNING CONTAINER -> m = docker run --rm -it -p 8888:8888 -v "$(pwd)":/app python-machine-learning | w = docker run --rm -it -p 8888:8888 -v ${PWD}:/app python-machine-learning

# Base image
FROM python:3.11-slim

# Working directory
WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Expose Jupyter port
EXPOSE 8888

# Default: run JupyterLab
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--allow-root", "--no-browser"]