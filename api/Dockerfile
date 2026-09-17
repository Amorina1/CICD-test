FROM python:3.12-slim

WORKDIR /app

RUN groupadd -r appgroup && useradd -r -g appgroup appuser

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt
 
COPY . .
 
USER appuser

EXPOSE 5000
 
CMD ["python", "app.py"]
