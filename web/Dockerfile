FROM tiangolo/uvicorn-gunicorn-fastapi:python3.9
WORKDIR /app
COPY src/requirements.txt .
RUN pip install -r requirements.txt

COPY src/main.py .
CMD ["uvicorn","main:app","--whost","0.0.0.0", "--port", "8000"]