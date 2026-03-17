# People Detection – Asynchronous Image Processing System

![Output: detected persons with bounding boxes](shared/results/4c98d512-ac26-4c5c-ac2d-24105c2f02bc.jpg)

This project implements an asynchronous system for detecting people in images using a microservice-like architecture.

The system uses a REST API, RabbitMQ message queue, and multiple worker services to process images in parallel. Object detection is performed using the YOLO (Ultralytics) model.

The main goal of the project is to demonstrate scalable and non-blocking processing of computationally expensive tasks.

## Architecture

* API service receives image requests (file upload or URL)
* Requests are sent to RabbitMQ queue
* Worker services consume tasks asynchronously
* Each worker performs person detection using YOLO
* Results are stored and returned via status endpoint

## Features

- Asynchronous image processing using RabbitMQ
- Scalable worker architecture (configurable number of workers)
- REST API for submitting and tracking jobs
- Support for image upload and URL-based processing
- Object detection using YOLO (Ultralytics)
- Dockerized services (API + workers)

## How it works

1. User sends request with image (local path, URL, or file upload)
2. API generates task_id and stores task metadata
3. Task is sent to RabbitMQ queue
4. Worker consumes task and runs YOLO detection
5. Results are stored and can be retrieved via task_id

## Tech Stack

Python, Flask, RabbitMQ, Docker, YOLO (Ultralytics)
