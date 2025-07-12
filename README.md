# DevOps Python Flask CICD

This is a sample DevOps project that demonstrates how to containerize a simple Flask application and deploy it to a Kubernetes cluster using CI/CD practices.

## 🔧 Tech Stack

- Python 🐍
- Flask 🌐
- Docker 🐳
- Kubernetes ☸️ (via Kind)
- GitHub 💻

## 🚀 Project Structure

devops-python-flask-cicd/
├── app.py # Flask application
├── Dockerfile # Container build file
├── requirements.txt # Python dependencies
├── config.yml # Kind cluster config (port mappings)
├── namespace.yml # Kubernetes namespace
├── flask-deployment.yaml # Kubernetes Deployment
├── service.yml # Kubernetes Service

## ▶️ Run Locally (for testing)

# Build Docker image
docker build -t flask-app .

# Run the Flask app
docker run -p 5000:5000 flask-app
Visit: http://localhost:5000

📦 Kubernetes Deployment (via Kind)

# Create Kind cluster
kind create cluster --config config.yml

# Create namespace
kubectl apply -f namespace.yml

# Deploy app and service
kubectl apply -f flask-deployment.yaml
kubectl apply -f service.yml

# Port Forward (optional)
kubectl port-forward svc/flask-service 5000:5000 -n flask
🧪 Sample Output

Hello from DevOps Pipeline!

📝 Author
Tanuj Saini
🔗 GitHub
