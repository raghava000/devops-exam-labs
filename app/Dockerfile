FROM python:3.10-slim AS test-env
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
Expose 8080
RUN pytest -q

FROM python:3.10-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dire -r requirements.txt
COPY app.py .
Expose 8080
CMD ["python", "app.py"]

