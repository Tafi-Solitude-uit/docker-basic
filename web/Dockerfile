FROM python:3.10

COPY requirements.txt requirements.txt

RUN python -m pip install --upgrade pip && python -m pip install -r requirements.txt

COPY . .

# Thiết lập lệnh khởi động ứng dụng web
CMD ["gunicorn", "-w", "2", "-b", ":8080", "app:app"]