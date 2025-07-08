# Clinic Agent (Doctor Appointment Multi-Agent System)
A conversational AI-powered multi-agent system that simulates patient-agent and scheduling-agent collaboration for automated doctor appointment booking.

🔗 **Overview**
This repository implements Clinic Agent: a modular, Python‑based multi-agent framework using LangChain and OpenAI LLMs. Each agent performs specialized tasks—such as patient interaction, doctor availability lookup, and appointment confirmation—to deliver a seamless booking experience via natural language conversations.

🧭 **Features**
Patient Agent
Initiates and guides the conversation with the user to gather required information (e.g. symptoms, preferred time slots, doctor specialization).

Doctor Availability Agent
Checks available doctors from a directory or simulated dataset; handles schedule constraints.

Appointment Scheduler Agent
Manages booking logic—reserves slots, generates confirmations, handles conflicts or rescheduling flows.

Conversation Coordinator
Orchestrates agent interactions and context flow to ensure smooth handoffs and comprehensive dialogue management.

🚀 **Installation**
Clone the repository:

```bash
git clone https://github.com/vinaykadam007/Doc-clinic-agent.git
cd doctor-appoitment-multiagent
Set up Python environment:
```

```bash
python3 -m venv venv
source venv/bin/activate
Install required libraries:
```

```bash
pip install -r requirements.txt
Configure your OpenAI API keys & other agent parameters via .env (copy from .env.example):
```

```text
OPENAI_API_KEY=your_openai_api_key_here
```

⚙️ **Usage**
Run the agent orchestration script to start the booking flow:

```bash
python main.py
Interact through console prompts (or integrate with a UI layer)—enter symptoms, view suggested doctors and slots, confirm appointment, receive confirmation output.
```

📂 **Repository Structure**
```bash
.
├── main.py              # Entry point orchestrating agents
├── patient_agent.py     # Patient interaction logic
├── availability_agent.py# Doctor lookup & availability logic
├── scheduler_agent.py   # Booking/rescheduling logic
├── requirements.txt
├── .env.example         # Sample environment configuration
└── README.md            # Project documentation
```

🧑‍💻 **Example Session**
```less
[PatientAgent] Hello! What health concern or specialty would you like to consult today?
> I have a fever and sore throat.

[AvailabilityAgent] Found Dr. Smith, Dr. Lee, Dr. Patel. Available slots:…
> I prefer Dr. Lee at 3 PM tomorrow.

[SchedulerAgent] Booking confirmed!  
Appointment: Dr. Lee — 2025‑07‑08 at 15:00  
Confirmation ID: ABC123
```

⚙️ **Extensibility & Customization**
Add new agents (e.g. InsuranceCheckerAgent, BillingAgent)

Swap LLM backends or models in LangChain pipelines

Upgrade knowledge base to integrate real doctor directories or hospital databases

Connect to a front-end (e.g. Streamlit, Flask) for chat-based UI

✅ **Benefits**
Enables a natural-language interface for appointment booking

Demonstrates multi-agent coordination powered by LLMs

Modular, extensible architecture—easy to add new tasks or integrate external services

👥 **Contributors**
Project authored by Vinay Kadam

Open to community contributions—feel free to raise issues or submit pull requests
