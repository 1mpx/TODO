FROM python:3.11-slim
WORKDIR /app
COPY requerements.txt /app/
RUN pip install --upgrade pip -r requerements.txt
COPY . /app/
COPY ./entrypoint.sh /app/entrypoint.sh
RUN chmod +x /app/entrypoint.sh
ENTRYPOINT["/app/entrypoint.sh"]

#RUN python manage.py collectstatic --noinput
EXPOSE 8000
#CMD ["gunicorn", "todo_list.wsgi:application", "--bind", "0.0.0.0:8000"]
