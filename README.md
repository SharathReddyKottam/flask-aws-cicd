# Flask AWS CI/CD with Jenkins on EC2

Flask REST API automatically tested and deployed to AWS EC2 using Jenkins CI/CD pipeline triggered by GitHub webhooks.

## Tech Stack
- Python 3.12 + Flask
- pytest
- Docker
- Jenkins on AWS EC2
- GitHub Webhooks

## Pipeline Stages
1. Build → pip install
2. Test → pytest 2/2 passed
3. Dockerize → docker build
4. Run → docker run on port 5000

## Live URL
http://13.218.177.28:5000
