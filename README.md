# AI-Powered Yoghurt Customer Service Automation
To handle customers request on the different flavors of yoghurt

## Yoghurt Customer Service Automation & Centralized Dashboard

## Overview

This project demonstrates the design and implementation of an AI-driven customer service automation system for a yoghurt production and distribution business.

The solution automates customer support operations, complaint management, ticketing, sentiment analysis, escalation workflows, reporting, and centralized analytics using AI and workflow automation.

The objective is to reduce manual customer service effort, improve response times, provide operational visibility, and create a scalable support infrastructure powered by Artificial Intelligence.

---

## Business Problem

Customer service teams often face challenges such as:

- High volume of customer inquiries
- Delayed response times
- Manual complaint tracking
- Lack of centralized reporting
- Poor visibility into customer satisfaction
- Inefficient escalation processes

This solution addresses these challenges by introducing AI-powered automation and centralized reporting.

---

## Solution Architecture

```text
Customer Support Form
          │
          ▼
Google Forms
          │
          ▼
Google Sheets Trigger (n8n)
          │
          ▼
OpenAI Intent Detection
          │
          ▼
Sentiment Analysis
          │
          ▼
Request Classification
          │
          ▼
Business Logic Routing
          │
 ┌────────┼────────┐
 ▼        ▼        ▼
Trello   Gmail   Telegram
Tickets  Alerts  Notifications
 │
 ▼
Supabase Database
 │
 ▼
Google Sheets Analytics
 │
 ▼
Looker Studio Dashboard
```

---

## Visual Representation in n8n: The workflow
<img width="1220" height="660" alt="Screenshot (744)" src="https://github.com/user-attachments/assets/983a16c2-e645-41ad-bbc1-be48a07a643e" />


## Technologies Used

### Workflow Automation
- n8n

### Artificial Intelligence
- OpenAI GPT-4o

### Database
- Supabase

### Ticket Management
- Trello

### Notifications
- Gmail
- Telegram

### Reporting & Analytics
- Google Sheets
- Looker Studio

### Data Collection
- Google Forms

---

## Workflow Components

### 1. Customer Request Intake

Customers submit support requests through a Google Form.

Information collected includes:

- Full Name
- Email Address
- Phone Number
- Department
- Request Type
- Priority Level
- Issue Description

---

### 2. AI Intent Classification

OpenAI analyzes incoming customer requests and determines:

- Intent
- Sentiment
- Urgency
- Category
- Recommended Action

#### Intent Categories

| Intent | Description |
|----------|-------------|
| Complaint | Customer dissatisfaction |
| Inquiry | Information request |
| Refund Request | Refund-related issue |
| Escalation | Requires management attention |
| Delivery Issue | Delivery-related problem |

---

### 3. AI Sentiment Analysis

The workflow evaluates customer sentiment:

- Positive
- Neutral
- Negative

Negative sentiment requests are automatically escalated to management.

---

### 4. Automated Ticket Creation

Support tickets are automatically generated in Trello.

#### Trello Workflow

- New Tickets
- In Progress
- Escalated Cases
- Resolved Issues

---

### 5. Automated Notifications

The workflow sends notifications through:

#### Gmail

- Customer confirmation email
- Resolution updates

#### Telegram

- Urgent complaint alerts
- Escalation notifications
- Daily support summaries

---

### 6. Centralized Data Storage

#### Supabase

Stores:

- Customer records
- Support tickets
- Sentiment analysis results
- AI classifications
- Resolution status

#### Google Sheets

Stores:

- Dashboard metrics
- Ticket summaries
- Reporting data
- KPI calculations

---

### 7. Executive Dashboard

Looker Studio provides real-time business intelligence and operational monitoring.

#### Dashboard Metrics

- Total Support Requests
- Open Tickets
- Resolved Tickets
- Escalated Cases
- Customer Sentiment Trends
- Average Resolution Time
- AI Resolution Rate
- Department Performance
- Support Volume Trends

---

## n8n Workflow Design

### Trigger Layer

- Google Sheets Trigger

### AI Processing Layer

- OpenAI Chat Model
- Intent Classification Parser

### Business Logic Layer

- Switch Node
- IF Node

### Data Layer

- Supabase Node
- Google Sheets Node

### Notification Layer

- Gmail Node
- Telegram Node

### Ticket Management Layer

- Trello Node

### Reporting Layer

- Looker Studio

---

## AI Prompt Engineering

### Intent Classification Prompt

```text
Analyze this customer support message and determine:

Intent:
- complaint
- inquiry
- refund_request
- escalation
- delivery_issue

Sentiment:
- positive
- neutral
- negative

Urgency:
- low
- medium
- high

Category:
- delivery_issue
- product_quality
- billing
- refund
- general_inquiry

Recommended Action:
- respond_standard
- escalate_to_manager
- process_refund
- investigate_delivery

Return structured JSON only.
```

---

## Business Automation Flow

```text
Customer Submits Form
          ↓
Google Sheets Trigger
          ↓
OpenAI Intent Analysis
          ↓
Sentiment Detection
          ↓
Request Classification
          ↓
Create Trello Ticket
          ↓
Store Data in Supabase
          ↓
Update Google Sheets
          ↓
Send Gmail Notification
          ↓
Send Telegram Alert
          ↓
Update Looker Studio Dashboard
```

---

## Key AI Features

### Intent Detection

Automatically identifies customer requests and support needs.

### Sentiment Analysis

Detects customer emotions and prioritizes critical issues.

### Automated Ticketing

Creates and manages support tickets automatically.

### Intelligent Escalation

Routes urgent cases to management without manual intervention.

### AI Analytics

Generates operational insights and performance recommendations.

---

## Business Value Delivered

- Faster customer response times
- Reduced manual workload
- Automated complaint management
- Improved customer satisfaction
- Centralized operational visibility
- Data-driven decision making
- Scalable support infrastructure

---

## Future Enhancements

- WhatsApp Integration
- Voice AI Support
- AI Knowledge Base (RAG)
- Multi-language Customer Support
- Predictive Customer Analytics
- AI Agents for Autonomous Resolution

---

## Skills Demonstrated

- AI Automation Engineering
- Workflow Orchestration
- Prompt Engineering
- Process Automation
- Data Engineering
- API Integration
- Dashboard Development
- Business Intelligence
- Customer Experience Automation
- Enterprise System Design

---

## Repository Structure

```text
.
├── README.md
├── workflows/
│   └── ai-yoghurt-customer-service.json
├── screenshots/
│   ├── workflow-canvas.png
│   ├── trello-ticket.png
│   ├── supabase-table.png
│   └── dashboard.png
├── docs/
│   ├── architecture.md
│   ├── prompts.md
│   └── workflow-design.md
```

---

## Author

**Godswill Umoh**

Machine Learning Engineer | AI Engineer | AI Automation Specialist

This project was developed to demonstrate enterprise-grade AI-powered customer service automation, workflow orchestration, centralized reporting, and business process optimization using n8n and modern AI technologies.
