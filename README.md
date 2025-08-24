# 🏥 Patient Management System
🔁 **Patient Management System** A web-based application built with **FastAPI** and **Streamlit**, utilizing a machine learning model stored in a Python pickle file to manage and predict patient outcomes based on medical data.

---

## 🧾 Project Overview
This project implements a **Patient Management System** using a machine learning model to predict **patient health outcomes**.  
It integrates a pre-trained model saved as a **pickle file**, offering a **user-friendly interface** via Streamlit and a **robust backend** with FastAPI.  
💡 **Use Cases:** Hospital Patient Monitoring, Medical Record Management, Predictive Health Analytics.

---

## 🧠 Tech Stack
<table> 
<tr> <th>Category</th> <th>Tool</th> <th>Usage</th> </tr> 
<tr> <td><strong>Programming Language</strong></td> <td><img src="https://cdn.worldvectorlogo.com/logos/python-5.svg" alt="Python" width="30"/> <strong>Python</strong></td> <td>Base language for model integration, preprocessing, and app logic</td> </tr> 
<tr> <td><strong>Web Framework</strong></td> <td><img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI" width="30"/> <strong>FastAPI</strong></td> <td>Backend framework for API development and deployment</td> </tr> 
<tr> <td><strong>Web App</strong></td> <td><img src="https://streamlit.io/images/brand/streamlit-logo-primary-colormark-darktext.png" alt="Streamlit" width="30"/> <strong>Streamlit</strong></td> <td>Framework to build and deploy an interactive web app for predictions</td> </tr> 
<tr> <td><strong>Model Storage</strong></td> <td><img src="https://upload.wikimedia.org/wikipedia/commons/0/0a/Python.svg" alt="Pickle" width="30"/> <strong>Pickle</strong></td> <td>Stores the trained machine learning model for predictions</td> </tr> 
</table>

---

## 🗂️ Project Structure
```
├── app.py # Streamlit web app
├── main.py # FastAPI backend
├── model.pkl # Trained machine learning model
├── patients.json # Patient data
├── requirements.txt # Python dependencies
└── README.md # Project documentation
```

---

## 🚀 Running the Application
Clone the repository, install dependencies, and launch the backend and frontend:

```bash
git clone https://github.com/ajitaiml/Patient-Management-System.git
cd Patient-Management-System
pip install -r requirements.txt
uvicorn main:app --reload  # Launch backend
streamlit run app.py       # Launch frontend

🎯 Key Features

🏥 Hospital Patient Monitoring

📋 Medical Record Management

🔍 Predictive Health Analytics

📄 License

This project is licensed under the GPL-3.0 License.

👤 Author
Ajit Singh
🔗 GitHub
