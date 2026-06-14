# MediSynapse AI: Intelligent Healthcare Coordination System

🚀 **Transforming Episodic Medical Appointments into Continuous, Secure, and Automated Care Loops.**

Developed as a flagship project for the **Software Design & Analysis** course by **Behzad Khan (24F-0575)** & **Subhan Yousaf (24F-0820)**.

---

## 📌 Project Overview
The contemporary healthcare ecosystem in emerging markets remains deeply fragmented. Patients face single-ended, episodic clinical visits where pre-consultation triage is non-existent, and post-consultation adherence monitoring drops off entirely after they leave the clinic. This results in high hospital readmission rates, disjointed medical histories, and administrative burnout for clinicians.

**MediSynapse AI** bridges this gap by acting as an end-to-end Intelligent Healthcare Coordination platform. By embedding NLP-driven triage, an automated dynamic recovery protocol engine, and an encrypted privacy vault, the platform establishes a true **"Continuity of Care."**

---

## ✨ Core Product Features

### 1. Intelligent Triage & Discovery Engine
* **Natural-Language Processing:** Accepts unstructured text/voice symptom descriptions from patients.
* **Risk Stratification:** Classifies conditions into **Green/Yellow/Red** triage tags using a custom machine learning architecture.
* **Smart Doctor Mapping:** Recommends and dynamically ranks healthcare providers based on specialization, real-time slot availability, and patient location.

### 2. Multi-Level Abstractive History Engine
* **LLM Compression Vault:** Summarizes sprawling, fragmented patient charts into a unified history pool.
* **Tiered Visibility:** Dynamically serves a **3-line critical snapshot** to physicians during emergency streams while keeping full, audited histories encrypted in the background.

### 3. Dynamic Follow-Up & Monitoring Engine
* **Automated Recovery Check-ins:** Allows doctors to provision specific vital thresholds (e.g., Temperature $> 102^\circ\text{F}$ or SpO2 $< 94\%$).
* **Proactive Threshold Breach Alerts:** Patients securely submit daily health metrics; if an entry breaches predefined safety levels, the system automatically fires off priority webhooks to notify the assigned physician immediately via Push/SMS.

### 4. Enterprise-Grade Security & Escrow
* **End-to-End Encryption (E2EE):** Encrypted signaling pipelines for virtual consults and messaging.
* **Escrow Financials:** Safeguards appointment payments in an escrow holding ledger, protecting both patient consumer rights and provider time until a consult is verified or an automated dispute handler resolves issues.

---

## 🛠️ Technical Architecture & Stack

MediSynapse AI utilizes a microservices-inspired, high-throughput backend paired with a mobile-first cross-platform client layer:

* **Frontend Client:** React Native (Mobile iOS/Android Apps) + Tailwind CSS
* **Core Application Backend:** Django (Python) for robust relational schemas, enterprise logic, and secure user sessions.
* **ML Inference Gateway:** FastAPI (Asynchronous Python endpoints for ultra-low latency model pipelines).
* **NLP & Artificial Intelligence Engine:** * BERT-based transformer classifier for triage mapping.
  * Fine-tuned Llama-3 / Hugging Face abstractive summarizers.
  * Vector Database embeddings utilizing FAISS / Pinecone for medical document querying.
* **Databases & Caching:** * PostgreSQL (Relational schema for transactional audits, financial escrows, and user roles).
  * MongoDB (Document store for dynamic, unstructured consultation summaries).
  * Redis (Fast state caching, session management, and rate-limiting queues).
* **Simulated Core Engine:** Standard compliant C++ execution environment implementing deterministic state machine sequences for critical transaction routes.

---

## 🗺️ System Design & Software Artifacts
*Note: UML diagrams can be inspected in detail within the assets folder or via your native `.drawio` viewer.*

The repository contains extensive Software Design & Analysis artifacts mapped explicitly from initial analysis down to structural code:
1. **Use Case Diagrams:** Defining strict boundaries for the *Patient*, *Doctor*, *Admin*, and *Third-Party Systems*.
2. **System Sequence Diagrams (SSDs):** Mapping step-by-step event lines, including financial escrow creation, biometric consent delegation, E2EE initiation, and real-time vital metrics threshold alerts.
3. **Core Architectural Trace:** Complete C++ sequence orchestration verifying that all multi-step workflows behave deterministically under heavy, multi-user simulation.

---

## 🚀 Getting Started

### Prerequisites
* Python 3.10+
* Node.js (v18+)
* C++20 Compliant Compiler (GCC/Clang)
* Docker & Docker Compose (Recommended for database spins)

### 📦 Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone [https://github.com/your-username/MediSynapse-AI.git](https://github.com/your-username/MediSynapse-AI.git)
   cd MediSynapse-AI

### Backend Setup (Django & FastAPI)

# Setup Virtual Environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install Dependencies
pip install -r requirements.txt

# Run Migrations & Start Servers
python manage.py migrate
python manage.py runserver 8000

### Frontend Setup (React Native Client)

bash
cd frontend
npm install
npm start

### Run the Core Orchestration Simulator (C++)

Bash
cd src/core_engine
g++ -std=c++20 main.cpp -o simulator
./simulator
