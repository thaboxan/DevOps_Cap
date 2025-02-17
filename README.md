# devops-qr-code

This is the sample application for my DevOps Capstone Project.
It generates QR Codes for the provided URL, the front-end is in NextJS and the API is written in Python using FastAPI.

## Application

**Front-End** - A web application where users can submit URLs.

**API**: API that receives URLs and generates QR codes. The API stores the QR codes in cloud storage(AWS S3 Bucket).

## Running locally

### API

The API code exists in the `api` directory. You can run the API server locally:

- Clone this repo
- Make sure you are in the `api` directory
- Create a virtualenv by typing in the following command: `python -m venv .venv`
- Install the required packages: `pip install -r requirements.txt`
- Create a `.env` file, and add you AWS Access and Secret key, check  `.env.example`
- Also, change the BUCKET_NAME to your S3 bucket name in `main.py`
- Run the API server: `uvicorn main:app --reload`
- Your API Server should be running on port `http://localhost:8000`

### Front-end

The front-end code exits in the `front-end-nextjs` directory. You can run the front-end server locally:

- Clone this repo
- Make sure you are in the `front-end-nextjs` directory
- Install the dependencies: `npm install`
- Run the NextJS Server: `npm run dev`
- Your Front-end Server should be running on `http://localhost:3000`

## DevOps Tools

- **Containerization**:  <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
- **CI/CD**: <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
- **Cloud Storage**: <img src="https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS S3 Bucket"/>
- **Infrastructure as Code**: <img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform"/>

## Goal

The goal is to get hands-on with DevOps practices like Containerization, CI/CD and monitoring

