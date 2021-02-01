# FROM ubuntu:18.04
# MAINTAINER your_name "email@gmail.com"
# RUN apt-get update -y
# RUN apt-get install -y python-pip python-dev build-essential
# COPY . /app
# WORKDIR /app
# RUN pip install -r requirements.txt
# ENTRYPOINT ["python"]
# CMD ["app.py"]


FROM python
MAINTAINER rupi "rupi@nemo-c.com"

WORKDIR /public_html/james
ADD ./requirements.txt /public_html/james/
RUN pip install -r requirements.txt

# RUN pip install flask && \
#     pip install flask_cors && \
#     pip install flask_apscheduler && \
#     pip install sqlalchemy && \
#     pip install pymysql && \
#     pip install celery && \
#     pip install requests && \
#     pip install scrapy && \
#     pip install flask_login && \
#     pip install flask_socketio && \
#     pip install eventlet && \
#     pip install dataset==1.3.0 && \
#     pip install xmltodict && \
#     pip install pillow && \
#     pip install gunicorn && \
#     pip install odin && \
#     pip install pyjwt && \
#     pip install datetimerange && \
#     pip install arrow && \
#     pip install selenium
#     # apt-get install -y firefox

EXPOSE 5000 5001

# ENTRYPOINT ["python"]
CMD ["python", "wsgi.py"]
