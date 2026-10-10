FROM python:3.11-slim-bookworm

WORKDIR /app

# Upgrade system packages to patch known base OS vulnerabilities
RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 5002
CMD ["python", "app.py"]