# LANGKAH KE-1
# Build image, jika sudah maka ngga perlu di build lagi
# docker build -t python-machine-learning .

# LANGKAH KE-2
# Running Container. pastikan nama buildnya sesuai. ini akan menghapus container setelah keluar
# m docker run --rm -it -p 8888:8888 -v "$(pwd)":/app python-machine-learning bash
# w docker run --rm -it -p 8888:8888 -v "${PWD}:/app" python-machine-learning bash

# LANGKAH KE-3
# Menjalankan Jupyter Notebook Di Browser, nanti buka link http://127.0.0.1:8888
# jupyter notebook --ip=0.0.0.0 --port=8888 --allow-root --no-browser

# Gunakan base image resmi
FROM python:3.11-slim

# SET working directory di dalam container
WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Default command (bisa diubah saat docker run)
CMD ["python", "app.py"]