# MCA Semester I - Practical 8: REST API Development & Automated Testing with FastAPI
**Course:** Python & Relational Programming  
**Student:** Sahil Surendra Shirke  

## Overview
Built a RESTful **Student Management API** using **FastAPI** and **Pydantic** (`main.py`) with automated endpoint and validation testing via **Pytest** and `TestClient` (`test_main.py`).

## Implemented Endpoints & Status Codes
- `GET /` — Health check returning `{"message": "Student API is running"}` (`200 OK`)
- `GET /students` — Retrieves all stored student records (`200 OK`)
- `POST /students` — Validates input (`name >= 2 chars`, `0 <= marks <= 100`), prevents duplicate `roll_no` (`409 Conflict`), and creates a new student (`201 Created`)
- `GET /students/{student_id}` — Retrieves a specific student by ID or raises `404 Not Found`

## How to Run
    pytest -v
    uvicorn main:app --reload
