#  IDKSQL

### *Ask your data anything.*

> A bold, offline-first Natural Language Database Interface that lets you query and manipulate databases without writing SQL.

---

##  Overview

**IDKSQL** is a full-stack system that allows users to interact with a PostgreSQL database using plain English.

Instead of writing SQL queries, users can simply type:

> “Show all training runs where loss > 1”
> “Add employee John age 28 salary 45000”

…and the system will:

1. Convert it into SQL
2. Execute it on the database
3. Return results
4. Explain what happened

---


##  Features

*  **Natural Language → SQL (offline using LLM)**
*  **Full CRUD support**

  * SELECT (Read)
  * INSERT (Create)
  * UPDATE (Modify)
  * DELETE (Remove)
*  **Real-time query execution on PostgreSQL**
*  **Query explanation in plain English**
*  **Chat-based interface with memory**
*  **Offline-first (no external APIs required)**
*  **SQL validation & safety checks**

---

##  Tech Stack

### Frontend

* React
* Custom CSS (dark, bold UI)

### Backend

* Node.js (Express)

### Database

* PostgreSQL

### AI / LLM

* Ollama (local runtime)
* LLaMA 3 (or compatible local model)

---

##  Architecture

```text
User (Natural Language)
        ↓
Frontend (React UI)
        ↓
Backend (Express API)
        ↓
Ollama (LLM → SQL)
        ↓
SQL Validation Layer
        ↓
PostgreSQL Database
        ↓
Results + Explanation
        ↓
Frontend Display
```

---

##  Installation

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/idksql.git
cd idksql
```

---

### 2. Install dependencies

#### Backend:

```bash
npm install express pg axios cors
```

#### Frontend:

```bash
npm install
```

---

### 3. Setup PostgreSQL

* Create your database
* Import schema from DA2
* Update credentials in backend config

---

### 4. Install Ollama

Download and install:
 https://ollama.com

Run model:

```bash
ollama run llama3
```

---

### 5. Start backend

```bash
node server.js
```

---

### 6. Start frontend

```bash
npm run dev
```

---

##  Example Queries

* “Show all training runs”
* “Find runs where loss > 1”
* “Add employee John age 28 salary 45000”
* “Update salary of John to 60000”
* “Delete employee John”

---

##  Safety Features

* Blocks dangerous queries (DROP, ALTER, TRUNCATE)
* Requires conditions for UPDATE/DELETE
* Validates SQL before execution

---

##  Project Structure

```text
IDKSQL/
├── frontend/
│   ├── components/
│   ├── pages/
│   └── App.jsx
│
├── backend/
│   ├── server.js
│   ├── db.js
│   ├── llm.js
│   └── utils/
│
├── database/
│   └── schema.sql
│
└── README.md
```

---

##  How It Works

1. User enters natural language query
2. Backend sends query to local LLM (Ollama)
3. LLM generates SQL
4. SQL is validated for safety
5. Query is executed on PostgreSQL
6. Results + explanation are returned

---

##  Limitations

* Accuracy depends on prompt quality and schema clarity
* Complex queries may require refinement
* LLM may occasionally generate incorrect SQL

---

##  Future Improvements

* Query suggestions / autocomplete
* Visual query builder
* Multi-database support
* Fine-tuned SQL model

---

##  Author

Built by [Your Name]

---

##  Final Note

IDKSQL is not just a database project —
it’s a step toward the future where:

> Humans talk.
> Systems understand.

---
