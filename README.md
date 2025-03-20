# ENGCE301 - Final LAB Solution

This is our Solution for the Final LAB in ENGCE301 Class

## 📋 Overview Web interface

<p align="center">
  <img src="Document/image/UIWEB_Wallboard.gif" alt="Wallboard Interface" width="80%">
</p>

## 📚 API Specification Documentation

📑 [View Complete API Documentation](./Document/README.md)

## ✅ Test Cases

### Agent Notification

| Test ID | Description | Test Steps | Expected Results | Actual Results |
|:-------:|:------------|:-----------|:----------------|:---------------|
| **R 1.1** | **Login Authentication** | 1. Navigate to login page<br>2. Enter valid username and password<br>3. Click login button | System grants access if credentials are valid | System granted access as expected |
| **R 1.2** | **Login/Logout Record Keeping** | 1. Login to the system<br>2. Logout from the system<br>3. Check activity logs | Login and logout activities are recorded with correct timestamps | Records are complete and timestamps are accurate |
| **R 1.3** | **Status Change History** | 1. Login to the system<br>2. Change agent status<br>3. Review status logs | Status changes are recorded with start and end times | Status changes completely recorded |
| **R 1.4** | **Agent Conversation Logging** | 1. Initiate chat<br>2. Send and receive multiple messages<br>3. Check chat history | System records all conversation messages | All conversation messages recorded |

### Agent Wallboard

| Test ID | Description | Test Steps | Expected Results | Actual Results |
|:-------:|:------------|:-----------|:----------------|:---------------|
| **R 2.1** | **Wallboard Banner Display** | 1. Navigate to Wallboard page<br>2. Verify banner appears correctly | Banner displays according to configured settings | Banner displayed as configured |
| **R 2.2** | **Login/Logout and Status History Display** | 1. Navigate to Wallboard page<br>2. Review login, logout and status history | All history displayed correctly | History data displayed completely and accurately |
| **R 2.3** | **Agent Conversation History Display** | 1. Navigate to Wallboard page<br>2. View agent chat history | All conversation history displayed correctly | Conversation history displayed completely |

## 📊 Data Flow Diagrams

<p align="center">
  <img src="Document/image/DataFlowDiagrams.gif" alt="Data Flow Diagrams" width="720">
</p>

## 🗃️ ER Diagrams

<p align="center">
  <img src="Document/image/ERDiagram.gif" alt="ER Diagram" width="720">
</p>

## 🔄 Activity Flow Diagram

```mermaid
stateDiagram
  direction LR
  [*] --> Still
  Still --> Moving
  Moving --> Crash:Send / Recieve Mesaage
  [*] --> s1
  s2 --> Crash:Login / Logoutgett Agent / UpdateAgent
  Crash --> s3
  s3 --> Crash
  s4 --> s5
  s5 --> s6
  s6 --> s5
  s6 --> Crash:UpdateAgentstatus
  s6 --> s7
  s7 --> s6
  s1 --> s2
  Still:PC (Agent)
  Moving:Agent-Notification
  Crash:Endpoint-api
  s1:PC (Agent)
  s2:Agent-Notification
  s3:MS SQL
  s4:PC<br>(Master)
  s5:Wallboard-fe
  s6:Parse-Server
  s7:MongoDB
```

## 👥 Our Team

| Profile | Name | Student ID | Role |
|:-------:|:-----|:-----------|:-----|
| <img src="https://avatars.githubusercontent.com/u/108066406?v=4" width="60" height="60" style="border-radius: 50%;" /> | Papon Saejar | 65543206021-9-7 | System Analyst & Tester |
| <img src="https://avatars.githubusercontent.com/u/108041952?v=4" width="60" height="60" style="border-radius: 50%;" /> | Sarayut Meepanya | 65543206037-5 | Team Leader & Developer |

## 📁 Our Team GitHub Repository

Visit Sarayut project repository: [Github-SarayutMI](https://github.com/SarayutMI)

Visit Papon project repository: [Github-Paponsaeja](https://github.com/Paponsaeja)

---
<p align="center">
  <i>Submitted March 2025 • Department of Computer Engineering</i>
</p>