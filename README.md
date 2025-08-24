Patient Management System (PMS)
📄 Description
The Patient Management System (PMS) is a robust and efficient API designed to streamline the management of patient records, appointments, and medical histories. Built with FastAPI and Python, this system provides a high-performance backend solution for healthcare providers to maintain accurate and accessible patient data. It emphasizes ease of use, scalability, and data integrity, making it a reliable tool for any medical practice.

✨ Features
Patient Management:

Add new patient records (name, contact, date of birth, gender, etc.).

View detailed information for individual patients.

Update existing patient details.

Delete patient records.

Search and filter patients by various criteria (e.g., name, ID).

Appointment Scheduling:

Create, view, update, and delete appointments.

Link appointments to specific patients and doctors.

Manage appointment status (scheduled, completed, cancelled).

Medical Records & History:

Record and retrieve medical conditions, diagnoses, treatments, and prescriptions.

Attach documents or notes to patient histories.

FastAPI & Pydantic: Leverages FastAPI for building high-performance APIs and Pydantic for data validation and serialization, ensuring robust and type-safe data handling.

Modular Design: Organized into logical modules for better maintainability and extensibility.

🚀 Technologies Used
Python 3.x: The core programming language.

FastAPI: High-performance web framework for building APIs.

Pydantic: Data validation and settings management using Python type hints.

Uvicorn: ASGI server for running FastAPI applications.

(Optional) SQLAlchemy: SQL toolkit and Object-Relational Mapper (ORM) for database interaction.

(Optional) PostgreSQL/SQLite: Database for storing patient and appointment data.

(Optional) Docker: For containerization and easier deployment.

🛠️ Installation
Follow these steps to get your Patient Management System up and running locally.

1. Clone the repository
git clone https://github.com/your-username/patient-management-system.git
cd patient-management-system

2. Create a Python Virtual Environment
It's recommended to use a virtual environment to manage dependencies.

python -m venv venv

3. Activate the Virtual Environment
On Windows:

.\venv\Scripts\activate

On macOS/Linux:

source venv/bin/activate

4. Install Dependencies
Install all required Python packages using pip.

pip install -r requirements.txt

(If you don't have a requirements.txt file yet, you can generate one after installing all packages like this: pip freeze > requirements.txt)

Example requirements.txt content:

fastapi==0.103.1
uvicorn==0.23.2
pydantic==2.4.2
# Add other dependencies like sqlalchemy, psycopg2-binary, etc., if used

5. Database Setup (if applicable)
If you're using a database like PostgreSQL or SQLite, you might need to:

For SQLite: No extra setup is usually needed as it's file-based.

For PostgreSQL: Ensure PostgreSQL is installed and running. Create a database and user if necessary. Update your database connection string in your application's configuration (e.g., in a .env file or config.py).

🏃 Usage
1. Run the FastAPI Application
Once all dependencies are installed and your virtual environment is active, you can run the application using Uvicorn.

uvicorn main:app --reload --host 0.0.0.0 --port 8000

main:app: Refers to the app object in your main.py file. Adjust main if your primary FastAPI file has a different name.

--reload: Enables auto-reloading of the server on code changes (useful for development).

--host 0.0.0.0: Makes the server accessible from other devices on the network.

--port 8000: Specifies the port to run the server on.

You should see output similar to this:

INFO:     Will watch for changes in these directories: ['/path/to/patient-management-system']
INFO:     Uvicorn running on http://0.0.0.0:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [xxxxx] using StatReload
INFO:     Started server process [xxxxx]
INFO:     Waiting for application startup.
INFO:     Application startup complete.

2. Access the API Documentation
Open your web browser and navigate to:

Interactive API Documentation (Swagger UI): http://localhost:8000/docs

Alternative API Documentation (Redoc): http://localhost:8000/redoc

Here you can see all available endpoints, their expected inputs, and try them out directly.

3. Example API Endpoints (via http://localhost:8000/docs)
GET /patients: Retrieve a list of all patients.

GET /patients/{patient_id}: Get details for a specific patient.

POST /patients: Create a new patient record.

Request Body Example:

{
  "name": "John Doe",
  "date_of_birth": "1990-05-15",
  "gender": "Male",
  "contact_number": "123-456-7890",
  "email": "john.doe@example.com",
  "address": "123 Main St, Anytown"
}

PUT /patients/{patient_id}: Update an existing patient's details.

DELETE /patients/{patient_id}: Remove a patient record.

GET /appointments: Get a list of all appointments.

POST /appointments: Schedule a new appointment.

Request Body Example:

{
  "patient_id": "patient_uuid_here",
  "doctor_name": "Dr. Jane Smith",
  "appointment_datetime": "2025-09-01T10:00:00",
  "reason": "Routine Checkup"
}

📂 Project Structure (Example)
A typical structure for a FastAPI project might look like this:

patient-management-system/
├── main.py                     # Main FastAPI application entry point
├── requirements.txt            # Python dependencies
├── .env                        # Environment variables (e.g., database URL)
├── app/
│   ├── __init__.py
│   ├── models/                 # Pydantic models for request/response bodies, database models (if using ORM)
│   │   ├── patient.py
│   │   ├── appointment.py
│   │   └── medical_record.py
│   ├── crud/                   # Create, Read, Update, Delete operations for database
│   │   ├── patient.py
│   │   ├── appointment.py
│   │   └── medical_record.py
│   ├── database/               # Database connection, session management
│   │   ├── connection.py
│   │   └── base.py
│   ├── routers/                # FastAPI routers for different API endpoints (e.g., /patients, /appointments)
│   │   ├── patients.py
│   │   ├── appointments.py
│   │   └── medical_records.py
│   └── services/               # Business logic, helpers
└── tests/                      # Unit and integration tests
    ├── test_patients.py
    └── test_appointments.py

🤝 Contributing
Contributions are welcome! If you'd like to contribute, please follow these steps:

Fork the repository.

Create a new branch (git checkout -b feature/your-feature-name).

Make your changes and ensure tests pass.

Commit your changes (git commit -m 'Add new feature').

Push to the branch (git push origin feature/your-feature-name).

Open a Pull Request.

