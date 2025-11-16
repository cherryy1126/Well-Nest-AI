🩺 Health and Wellness Assistant

A multi-agent system designed to help users manage their health-related tasks, from scheduling appointments to monitoring health metrics and managing medications. This system leverages the Azure AI Agent Service, Semantic Kernel, and a deterministic process framework for robust, reliable, and intelligent collaboration.

🎯 Core Features

🤖 Multi-Agent Collaboration: Domain-specific agents (e.g., Nutrition, Medication, Appointments) work together to address comprehensive health needs.

⚙️ Deterministic Workflows: A structured process framework ensures reliable and predictable agent interactions, which is critical for health applications.

📞 Dynamic Function Calling: Agents can perform concrete, real-world actions (like booking appointments) through an integrated OpenAI function calling framework.

❤️ Comprehensive Health Management: The system covers a wide range of domains:

Nutrition & Meal Planning

Medication Reminders & Adherence

Appointment Scheduling

Health Metric Monitoring (from devices)

Mental Health Support

Emergency Response Coordination

💡 Use Cases

Our solution is designed for individuals managing their personal health or for caregivers supporting others.

Chronic Disease Management: Helping patients track medications, appointments, and key health metrics for conditions like diabetes or hypertension.

Preventive Health: Supporting users in maintaining healthy habits through nutrition guidance, supplement tracking, and scheduling regular check-ups.

Care Coordination: Assisting elderly individuals or their caregivers in managing complex healthcare needs across multiple providers and systems.

🛠️ System Architecture & Implementation

The Health and Wellness Assistant is implemented as a modular system. The architecture is designed to be scalable, maintainable, and robust, with clear separation of concerns.

Each domain agent focuses on a specific health vertical.

The orchestrator manages the flow of information and tasks between agents.

The process framework ensures deterministic, step-by-step collaboration for complex tasks.

The function calling framework provides agents with tools to interact with external systems and data.

Data files provide structured information and knowledge for the agents to operate on.

Key Integration Points

Agent Orchestration: The orchestrator routes requests to appropriate domain agents based on user needs and context.

Function Calling: Agents call registered functions (e.g., get_appointments, book_appointment) to perform actions.

Workflow Management: Complex tasks (like "manage my diabetes plan") are broken down into managed workflows with defined steps and decision points.

Azure OpenAI API: Provides the core intelligence for agents, enabling them to understand requests and generate appropriate responses.

Semantic Kernel (Optional): Enhances capabilities with structured prompting, memory, and specialized skills where integrated.

📁 Directory Structure

.
├── 📂 agents/
│   ├── appointment_agent.py
│   ├── care_coordination_agent.py
│   ├── emergency_response_agent.py
│   ├── health_metrics_agent.py
│   ├── medication_agent.py
│   ├── mental_health_agent.py
│   └── nutrition_agent.py
├── 📂 data/
│   ├── Appointments.json
│   ├── Care Coordination Data.json
│   ├── Health Metrics.json
│   ├── Healthcare Providers.json
│   ├── Medications.json
│   ├── Mental Health Data.json
│   ├── Nutrition Data.json
│   └── User Profiles.json
├── 📂 function_calling/
│   ├── function_registry.py
│   └── function_executor.py
├── 📂 orchestrator/
│   └── orchestrator_agent.py
├── 📂 process_framework/
│   ├── workflow_manager.py
│   └── workflow.py
├── 📂 semantic_kernel/
│   ├── sk_config.py
│   └── *_skills.py
├── 📂 ui/
│   ├── cli_ui_agent.py
│   └── api_ui_agent.py
├── 📂 utils/
│   ├── azure_ai_service.py
│   └── model_selector.py
├── .gitignore
├── .env
├── README.md
├── requirements.txt
└── main.py


🧩 Core Components

📄 Root Files

File

Description

.gitignore

Specifies files to exclude from version control (env files, pycache, etc.)

.env

Contains environment variables including Azure OpenAI API credentials

README.md

Project documentation with setup instructions and overview

requirements.txt

Lists project dependencies (openai, requests, tiktoken, etc.)

main.py

Entry point for the application that initializes and connects all components

1. 🤖 Domain-Specific Agents (/agents/)

Each agent specializes in a specific health domain.

Agent

Purpose

appointment_agent

Manages healthcare appointment scheduling

care_coordination_agent

Coordinates care across multiple providers

emergency_response_agent

Handles urgent health situations and alerts

health_metrics_agent

Monitors and analyzes health metrics from devices

medication_agent

Handles medication reminders and adherence tracking

mental_health_agent

Provides mental health support and monitoring

nutrition_agent

Manages dietary recommendations and meal planning

2. ☁️ Azure OpenAI Integration (/utils/)

Provides utilities for interacting with the Azure OpenAI API.

File

Purpose

azure_ai_service.py

Client for Azure OpenAI API interactions

model_selector.py

Selects appropriate models based on context and complexity

3. 📞 Function Calling Framework (/function_calling/)

Implements the core pattern for agents to call external functions.

File

Purpose

function_registry.py

Registers functions and generates OpenAI-compatible schemas

function_executor.py

Executes functions based on agent requests and handles results

4. ⚙️ Process Framework (/process_framework/)

Enables structured, deterministic workflows for multi-agent collaboration.

File

Purpose

workflow_manager.py

Manages multiple workflows and their execution states

workflow.py

Defines orchestrator/agent instructions and workflow steps

5. 🧑‍✈️ Orchestration (/orchestrator/)

Coordinates interactions between all agents and components.

File

Purpose

orchestrator_agent.py

Routes requests, manages workflows, and handles function calls

6. 🖥️ User Interfaces (/ui/)

Provides different interfaces for interacting with the system.

File

Purpose

cli_ui_agent.py

Command-line interface for the assistant

api_ui_agent.py

FastAPI-based web API for integration with other systems

7. 🧠 Semantic Kernel Integration (/semantic_kernel/)

Optional integration with Semantic Kernel for enhanced capabilities.

File

Purpose

sk_config.py

Configuration for Semantic Kernel

*_skills.py

Domain-specific skills for Semantic Kernel

8. 🗂️ Data Files (/data/)

Contains structured JSON data for the application.

File

Purpose

Appointments.json

Appointment data and scheduling information

Care Coordination Data.json

Care coordination across providers

Health Metrics.json

User health measurements and tracking

Healthcare Providers.json

Provider information and specialties

Medications.json

Medication information and schedules

Mental Health Data.json

Mental health tracking and resources

Nutrition Data.json

Nutritional information and meal plans

User Profiles.json

User profile information

🚀 Getting Started

Prerequisites

Python 3.8 or higher

Azure OpenAI API access

Azure AI Agent Service access

💾 Installation

Clone the repository:

git clone 
cd your-repository-name


Install dependencies:

pip install -r requirements.txt


Set up environment variables:

Copy the example environment file:

cp .env.example .env


Edit the .env file with your Azure OpenAI credentials (API key, endpoint, etc.).

Run the application:

python main.py
