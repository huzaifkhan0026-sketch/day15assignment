# Dockerized Python Application

This project demonstrates a simple Dockerized Python application using the official `python:3.12-slim` Docker image.

The application prints:

* Current Python version running inside the container
* Current date and time

---

## Project Structure

```text
docker-python-app/
│
├── app.py
├── Dockerfile
├── requirements.txt
├── README.md
└── screenshot.png
```

---

## Python Script (app.py)

```python
import sys
from datetime import datetime

print("Python Version:", sys.version)
print("Current Date & Time:", datetime.now())
```

---

## Dockerfile

```dockerfile
FROM python:3.12-slim

WORKDIR /app

COPY app.py .

CMD ["python", "app.py"]
```

---

## Requirements File (requirements.txt)

No external dependencies are required.

```text
# Empty file
```

---

## Build Docker Image

Run the following command from the project directory:

```bash
docker build -t python-version-app .
```

---

## Run Docker Container

```bash
docker run --rm python-version-app
```

---

## Sample Output

```text
Python Version: 3.12.11 (main, Jun  3 2025, 12:00:00) [GCC 12.2.0]

Current Date & Time: 2026-06-24 14:30:45.123456
```

---

## Screenshot

Add a screenshot of the output and save it as:

```text
screenshot.png
```

Then include it in the README:

```markdown
## Output Screenshot

![Output Screenshot](screenshot.png)
```

---

## Push Project to GitHub

### Initialize Git Repository

```bash
git init
git add .
git commit -m "Initial commit"
```

### Create GitHub Repository

Create a new repository on GitHub and connect it:

```bash
git remote add origin https://github.com/your-username/docker-python-app.git
git branch -M main
git push -u origin main
```

---

## Technologies Used

* Python 3.12
* Docker
* Git
* GitHub

---

## Author

Huzaif Ahmed Khan
