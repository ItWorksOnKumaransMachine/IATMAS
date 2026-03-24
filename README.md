# AI Training Memory and Analytics System

## Overview

NeuroVault is a full-stack system designed to store, manage, and analyze AI training processes using a structured relational database. It extends traditional database applications by incorporating real-time analytics, anomaly detection, and a web-based visualization layer.

---

## Objectives

* Design a normalized relational database for AI training data
* Implement database connectivity using a backend service
* Develop a front-end interface for user interaction
* Perform CRUD operations through a web application
* Provide analytical insights from stored data

---

## System Architecture

Frontend (HTML, Tailwind CSS)
→ Backend (Flask, Python)
→ PostgreSQL Database

Optional: Raspberry Pi for distributed data ingestion

---

## Technology Stack

* PostgreSQL (Relational Database)
* Flask (Backend Framework)
* psycopg2 (Database Connectivity)
* HTML + Tailwind CSS (Frontend)
* Chart.js (Data Visualization)

---

## Database Design

The system is based on a normalized schema (BCNF), including the following entities:

* MODEL
* MODEL_VERSION
* TRAINING_RUN
* EXECUTION_STEP
* METRIC_SCALAR
* DATASET
* RUN_DATASET_MAP

Additional tables:

* ALERT
* SYSTEM_LOG

---

## Features

### Database Operations

* Insert new training metrics
* Retrieve and display data
* Update metric values
* Delete records

### Visualization

* Line chart for loss trends
* Tabular representation of metrics

### Backend Integration

* REST-style routing using Flask
* Secure parameterized SQL queries

### Anomaly Detection

* Trigger-based alerts for abnormal values

---

## Setup Instructions

### Install Dependencies

pip install flask psycopg2

---

### Database Setup

1. Create database:

CREATE DATABASE aimemory;

2. Execute SQL scripts from previous phases

---

### Run Application

python app.py

---

### Access Interface

http://127.0.0.1:5000

---

## Project Structure

aimemory_da3/
│
├── app.py
├── templates/
│   ├── index.html
│   ├── insert.html
│   ├── update.html
│
├── static/
└── requirements.txt

---

## Future Work

* Real-time streaming using WebSockets
* Advanced anomaly detection using machine learning
* Authentication and user management
* Cloud deployment

---

## Author

C. Kumaran
B.Tech Computer Science (Data Science)
