
<img width="1114" height="502" alt="Screenshot 2025-11-16 184555" src="https://github.com/user-attachments/assets/4dd96f6f-6276-41f1-8bc0-d1d4a4667891" />



<img width="1092" height="530" alt="Screenshot 2025-11-16 184502" src="https://github.com/user-attachments/assets/86a8f040-82b2-4df8-8175-77b5899e4454" />



<img width="1124" height="526" alt="Screenshot 2025-11-16 184630" src="https://github.com/user-attachments/assets/61ce11ef-e6ff-429c-ba85-b144a6b13814" />



<img width="1078" height="840" alt="Screenshot 2025-11-16 184854" src="https://github.com/user-attachments/assets/91c8dcee-2cf2-4849-929b-0f910aa347c8" />



<img width="1430" height="829" alt="Screenshot 2025-11-16 185012" src="https://github.com/user-attachments/assets/d5099fa6-71e3-495a-967d-33b05a049329" />




<img width="1375" height="441" alt="Screenshot 2025-11-16 185046" src="https://github.com/user-attachments/assets/eb4bd318-81ab-4e52-bf46-3fa47de01e5b" />





---

## 🧩 Core Components

### 📄 Root Files

| **File**                | **Description**                                                             |
|-------------------------|-----------------------------------------------------------------------------|
| `.gitignore`            | Specifies files to exclude from version control (env files, pycache, etc.)  |
| `.env`                  | Contains environment variables including Azure OpenAI API credentials       |
| `README.md`             | Project documentation with setup instructions and overview                  |
| `requirements.txt`      | Lists project dependencies (openai, requests, tiktoken, etc.)               |
| `main.py`               | Entry point for the application that initializes and connects all components|

---

### 🤖 Domain-Specific Agents (`/agents/`)

Each agent specializes in a specific health domain.

| **Agent**               | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `appointment_agent`      | Manages healthcare appointment scheduling                                     |
| `care_coordination_agent`| Coordinates care across multiple providers                                    |
| `emergency_response_agent`| Handles urgent health situations and alerts                                  |
| `health_metrics_agent`   | Monitors and analyzes health metrics from devices                             |
| `medication_agent`       | Handles medication reminders and adherence tracking                           |
| `mental_health_agent`    | Provides mental health support and monitoring                                 |
| `nutrition_agent`        | Manages dietary recommendations and meal planning                             |

---

### ☁️ Azure OpenAI Integration (`/utils/`)

Provides utilities for interacting with the Azure OpenAI API.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `azure_ai_service.py`    | Client for Azure OpenAI API interactions                                     |
| `model_selector.py`      | Selects appropriate models based on context and complexity                   |

---

### 📞 Function Calling Framework (`/function_calling/`)

Implements the core pattern for agents to call external functions.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `function_registry.py`   | Registers functions and generates OpenAI-compatible schemas                    |
| `function_executor.py`   | Executes functions based on agent requests and handles results                |

---

### ⚙️ Process Framework (`/process_framework/`)

Enables structured, deterministic workflows for multi-agent collaboration.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `workflow_manager.py`    | Manages multiple workflows and their execution states                         |
| `workflow.py`            | Defines orchestrator/agent instructions and workflow steps                    |

---

### 🧑‍✈️ Orchestration (`/orchestrator/`)

Coordinates interactions between all agents and components.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `orchestrator_agent.py`  | Routes requests, manages workflows, and handles function calls                |

---

### 🖥️ User Interfaces (`/ui/`)

Provides different interfaces for interacting with the system.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `cli_ui_agent.py`        | Command-line interface for the assistant                                      |
| `api_ui_agent.py`        | FastAPI-based web API for integration with other systems                      |

---

### 🧠 Semantic Kernel Integration (`/semantic_kernel/`)

Optional integration with Semantic Kernel for enhanced capabilities.

| **File**                | **Purpose**                                                                   |
|-------------------------|-------------------------------------------------------------------------------|
| `sk_config.py`           | Configuration for Semantic Kernel                                             |
| `*_skills.py`            | Domain-specific skills for Semantic Kernel                                    |

---

### 🗂️ Data Files (`/data/`)

Contains structured JSON data for the application.

| **File**                | **Purpose**                                                                    |
|-------------------------|------------------------------------------------------------------------------- |
| `Appointments.json`      | Appointment data and scheduling information                                   |
| `Care Coordination Data.json`| Care coordination across providers                                        |
| `Health Metrics.json`    | User health measurements and tracking                                         |
| `Healthcare Providers.json`| Provider information and specialties                                        |
| `Medications.json`       | Medication information and schedules                                          |
| `Mental Health Data.json`| Mental health tracking and resources                                          |
| `Nutrition Data.json`    | Nutritional information and meal plans                                        |
| `User Profiles.json`     | User profile information                                                      |

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8 or higher**
- **Azure OpenAI API access**
- **Azure AI Agent Service access**

### 💾 Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <directory>
2. Install dependencies:

    pip install -r requirements.txt


3. Set up environment variables:

    Copy the example environment file:

    cp .env.example .env


Update .env with your Azure OpenAI API credentials and other environment variables.
