# Multi-Agent AI Business Automation Platform
A robust, self-hosted multi-agent AI automation platform built with **n8n**, **Ollama**, and **LangChain**. This system orchestrates 12 specialized AI agents to handle end-to-end business operations—from intelligent lead capture and customer support to automated sales pipelines, appointment booking, marketing campaigns, and governance.

##  System Architecture

The platform follows a structured execution pipeline:

1. **User Login & Onboarding:** When a new user logs in, the company onboarding triggers automatically.
2. **Intake & DNA:** An interactive intake form appears to capture and save critical business info, feeding into the Company DNA.
3. **Orchestration & Governance:** Every specialized agent is dynamically triggered, monitored, and routed through the central orchestration layer.

    NEW USER LOGIN                 
                  │                          
                  ↓                          
        COMPANY ONBOARDING                   
                  │                          
                  ↓                          
          INTAKE FORM & DNA                  
                  │                          
                  ↓                          
    ORCHESTRATION & GOVERNANCE               
                  │                          
    ┌─────────────┼─────────────┐            
    ↓             ↓             ↓            
  LEAD         SUPPORT         SALES         
    │             │             │            
    └─────────────┼─────────────┘            
                  ↓                          
           DATA & RESPONSES


## 🤖 The 12 Specialized Agents & Workflows

1. **Intake & DNA Steward:** Manages system-wide guidelines, prompt constraints, and dynamic company context retrieval.
2. **Lead Capture Agent:** Extracts contact details, region, and intent accurately from raw customer messages while enforcing strict JSON schemas.
3. **Customer Support Agent:** Handles Tier-1 customer queries using local vector data and Company DNA.
4. **Appointment Agent:** Automates meeting and consultation bookings via dedicated scheduling sub-workflows.
5. **Sales Agent:** Qualifies leads, evaluates conversion potential, and routes high-value prospects to human teams.
6. **Quote & Proposal Agent:** Generates custom service estimates and project scopes dynamically.
7. **Marketing Campaign Agent:** Automates outbound content generation, audience tracking, and campaign metrics.
8. **Follow-up Agent:** Schedules automated touchpoints and reminders for active leads.
9. **WhatsApp Engagement Agent:** Manages messaging webhooks and chat threads for real-time mobile interactions.
10. **Review & Feedback Agent:** Collects post-service evaluations and processes customer feedback metrics.
11. **Analytics & Insights Agent:** Aggregates database records to yield operational trends and performance reporting.
12. **Orchestration & Governance:** Oversees multi-agent handoffs, guardrails, error-handling, and human-in-the-loop triggers.

---

## Technology Stack

* **Workflow Automation:** n8n (Self-hosted)
* **Local LLM Engine:** Ollama (Running models like `qwen2.5:1.5b`)
* **Framework:** LangChain (n8n LangChain nodes)
* **Databases & Storage:** n8n Data Tables
* **Integrations:** REST APIs, Webhooks, SMTP Email, Pipedrive CRM

---

##  Local Setup & Installation

### Prerequisites
* [n8n](https://n8n.io/) installed locally (default running at `http://localhost:5678`)
* [Ollama](https://ollama.com/) installed locally with your preferred model (e.g., `ollama run llama3.2:3b`)

### Steps to Run
1. Clone this repository:
   ```bash
  git clone https://github.com/alaihanadeem/multi-agent-ai-automation-platform.git
