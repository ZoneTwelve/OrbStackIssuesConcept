FROM python:3.10.9-slim as builder 
ARG APP_NAME
ENV APP_NAME $APP_NAME
WORKDIR /src
COPY $APP_NAME .
RUN uname -a
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

FROM python:3.10.9-slim
WORKDIR /src
COPY --from=builder /src /src
COPY --from=builder /usr/local/lib/python3.10/site-packages /usr/local/lib/python3.10/site-packages

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]