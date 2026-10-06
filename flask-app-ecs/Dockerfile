# Base image (OS)

# FROM python:3.14-slim

# # Working directory

# WORKDIR /app

# # Copy src code to container

# COPY . .

# # Run the build commands

# RUN pip install -r requirements.txt

# # expose port 80

# EXPOSE 80

# # serve the app / run the app (keep it running)

# CMD ["python","run.py"]

# FROM python:3.11

# WORKDIR /app

# COPY . .

# RUN pip install -r requirements.txt

# ENTRYPOINT [ "python","run.py" ]

# stage 1 base image 1.62GB 416MB
FROM python:3.11 AS builder

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

#--------------------------------------
# stage 2 base image 220MB 52.3MB
FROM python:3.11-slim

WORKDIR /app

COPY --from=builder /usr/local/lib/python3.11/site-packages/ /usr/local/lib/python3.11/site-packages/

COPY . .
ENTRYPOINT [ "python","run.py" ]
