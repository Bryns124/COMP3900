# 1. We need to use the base image for `python:3.8-slim`. This is a small version of Python
FROM python:3.8-slim
# 2. Our working directory can simply be `/usr/src/app`
WORKDIR /usr/src/app
# 3. Next let's copy all files from `.` (current directory) into `.` (in the docker container)
COPY  . .
# 4. In Python we have a `requirements.txt` file which specifies all the required packages. We have provided that to you. You need to run `pip install --no-cache-dir -r requirements.txt` inside your container. This command uses `pip` which is Python's package manager to install all packages from `requirements.txt`
RUN pip install --no-cache-dir -r requirements.txt
# 5. Let the container know that we will be listening to port 5000
EXPOSE 5000
# 6. Specify the command to run the backend which is `python app.py` (make sure to double check the command you use to do this and its syntax)
CMD ["python", "app.py"]