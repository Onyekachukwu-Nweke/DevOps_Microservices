FROM python:3.7.3-stretch

#Working Directory
WORKDIR /app

#Copy Source code to working directory
COPY . flask_app/web.py /app/
COPY . nlib /app/

# Install packages frpm requirements.txt
# hadolint ignore=DL3013
RUN pip install --upgrade pip &&\
    pip install --trusted-host pypi.python.org -r requirements.txt

# Expose Port 80
EXPOSE 80

# Run app at container launch
CMD ["python", "web.py"]