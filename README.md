🚀 My Docker Projects

Welcome to my **Docker, Kubernetes, and ML Projects** repository! 🎯 This serves as a central hub for all my containerized projects, complete with step-by-step deployment guides.

---

## 📌 Technologies Used

✅ **Docker & Docker Compose** 🐳  
✅ **MySQL & PostgreSQL Databases** 🗄️  
✅ **Streamlit for UI** 📊  
✅ **ML Model Deployment & Monitoring** 🤖  
✅ **Kubernetes with Minikube & Kubectl** ⚙️  

---

## 📂 Project List

| 🔹 **Project** | 📌 **Description** | 🔗 **Repo Link** |
|--------------|----------------|-------------|
| **1️⃣ Docker Basics** | Learn fundamental Docker commands and concepts | [GitHub Repo](https://github.com/Shelly151/Docker_basics.git) |
| **2️⃣ Docker ML Mushroom Classifier** | Deploy an ML model for mushroom classification using Docker | [GitHub Repo](https://github.com/Shelly151/ML-Mushroom_Docker.git) |
| **3️⃣ MySQL using Docker** | Set up and run MySQL inside a Docker container | [GitHub Repo](https://github.com/Shelly151/MySQL_Docker.git) |
| **4️⃣ Docker Volume Persistence** | Persist data across containers using Docker volumes | [GitHub Repo](https://github.com/Shelly151/Docker_Volume.git) |
| **5️⃣ Docker Container Communication** | Set up container-to-container communication in Docker | [GitHub Repo](https://github.com/Shelly151/Docker_Network.git) |
| **6️⃣ Streamlit & PostgreSQL in Docker** | Deploy a Streamlit app connected to PostgreSQL using Docker | [GitHub Repo](https://github.com/Shelly151/Docker_Full-Stack.git) |
| **7️⃣ Minikube & Kubectl Lab** | Set up a local Kubernetes cluster and deploy apps | [GitHub Repo](https://github.com/Shelly151/Minikube-and-Kucetl.git) |
| **8️⃣ ML Model Deployment using Docker & EC2** | Deploy a Dockerized ML Model using Streamlit on AWS EC2 | [GitHub Repo](https://github.com/Shelly151/EC2-Streamlit.git) |
| **9️⃣ Titanic Survival** | Machine learning web application that predicts whether a passenger would have survived the Titanic disaster. | [GitHub Repo](https://github.com/Shelly151/titanic-survival.git) |
| **🔟 Evidential AI** | etting up an Evidently AI-based Streamlit application running inside a Docker container. | [GitHub Repo](https://github.com/Shelly151/Evidential-Ai.git) |



---

## 🔥 Project Details

### 1️⃣ Docker Basics 🐳  
📌 **Goal:** Learn essential Docker concepts, commands, and best practices.

🔹 **Topics Covered:**
- What is Docker?
- Installing Docker
- Running containers (`docker run`)
- Managing images (`docker pull`, `docker build`)
- Stopping & removing containers

📜 **Commands:**
```sh
docker run -it ubuntu bash
docker ps -a
docker images
docker stop container_id
docker rm container_id
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/Docker_basics.git)

---

### 2️⃣ Docker ML Mushroom Classifier 🍄🤖  
📌 **Goal:** Deploy an ML model that classifies mushrooms as edible or poisonous using Docker.

✅ Train the model using Scikit-Learn  
✅ Create a Flask API for inference  
✅ Containerize the model using Docker  

📜 **Setup:**
```sh
docker build -t mushroom-classifier .
docker run -p 5000:5000 mushroom-classifier
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/ML-Mushroom_Docker.git)

---

### 3️⃣ MySQL using Docker 🗄️  
📌 **Goal:** Run a MySQL database inside a Docker container.

📜 **Setup Commands:**
```sh
docker run --name mysql_container -e MYSQL_ROOT_PASSWORD=root -d mysql
docker exec -it mysql_container mysql -u root -p
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/MySQL_Docker.git)

---

### 4️⃣ Docker Volume Persistence 💾  
📌 **Goal:** Learn how to persist data across Docker containers.

🔹 **Key Concepts:**
✔ Bind Mounts (host-based persistence)  
✔ Docker Volumes (managed by Docker)  

📜 **Commands:**
```sh
docker run -v /mydata:/container_data ubuntu touch /container_data/sample.txt
docker inspect container_id | grep Mounts
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/Docker_Volume.git)

---

### 5️⃣ Docker Container Communication 🌐  
📌 **Goal:** Enable communication between multiple Docker containers using networking.

🔹 **Topics Covered:**
- Docker bridge networks
- Connecting multiple containers
- Inspecting network configurations

📜 **Commands:**
```sh
docker network create my_network
docker network connect my_network container1
docker inspect my_network
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/Docker_Network.git)

---

### 6️⃣ Streamlit & PostgreSQL in Docker 🎨📊  
📌 **Goal:** Deploy a Streamlit app connected to a PostgreSQL database using Docker.

📜 **Setup Commands:**
```sh
docker network create my_postgres_network
docker run --name my_postgres -e POSTGRES_USER=admin -e POSTGRES_DB=mydb -d postgres
docker build -t streamlit_app .
docker run --network my_postgres_network -p 8501:8501 -d streamlit_app
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/Docker_Full-Stack.git)

---

### 7️⃣ Minikube & Kubectl Lab 🏗️🔥  
📌 **Goal:** Set up and manage a Kubernetes cluster locally using Minikube & Kubectl.

📜 **Setup Commands:**
```sh
minikube start
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --type=NodePort --port=80
minikube service nginx --url
kubectl scale deployment nginx --replicas=3
kubectl delete service nginx
kubectl delete deployment nginx
```
🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/Minikube-and-Kucetl.git)

---

### 8️⃣ ML Model Deployment Using Docker & EC2 🐳🌍  
📌 **Goal:** Deploy a Dockerized ML Model and host it on AWS EC2.

📜 **Setup Commands:**
```sh
ssh -i /path/to/your-key.pem ec2-user@your-ec2-public-ip
sudo yum update -y
sudo yum install docker -y
sudo service docker start
sudo usermod -a -G docker ec2-user
exit  # Log out and log back in for changes to take effect
git clone https://github.com/Shelly151/EC2-Streamlit.git
cd ml-docker-app
docker build -t streamlit-app .
docker run -d -p 8501:8501 --name my-streamlit-app streamlit-app
sudo docker update --restart unless-stopped my-streamlit-app
```
📌 **Access the Web App:** 👉 Open your browser and visit `http://your-ec2-public-ip:8501`

🔗 **Repository:** [GitHub Repo](https://github.com/Shelly151/EC2-Streamlit.git)

---

🚀 **Happy Containerizing!** 🐳🎯

