<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" />
</p>

# osTicket — Post-Install Configuration

This repository documents the **post-install configuration steps** I performed for osTicket (Windows 10 / IIS environment).  
Each step includes a placeholder for a screenshot — replace the Imgur link with your uploaded image.

---

## Environments & Technologies Used
- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop (RDP)
- Internet Information Services (IIS)
- PHP, MySQL/MariaDB (as used by osTicket)

## Operating System
- **Windows 10 (21H2)**

---

## Post-Install Configuration Objectives
- Configure roles, departments, teams, agents, and users  
- Enforce registration requirements & user visibility  
- Configure SLAs, help topics, and basic security/hardening  
- Provide screenshot placeholders for documentation

---

### 1) Configure Agents (workers)
**Path:** `Admin Panel -> Agents -> Add New`  
**Action taken:** Created agents:  
- **Jane** — Department: SysAdmins  
- **John** — Department: Support

**Notes / Why:** Add agents and assign to departments for ticket handling and notifications.

<p align="center">
<img src="https://i.imgur.com/M4MUWev.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 2) Configure Roles (for grouping permissions)
**Path:** `Admin Panel -> Agents -> Roles`  
**Action taken:** Created role **Supreme Admin**.

**Notes / Why:** Use roles to group and manage permission sets for agents.

<p align="center">
<img src="https://i.imgur.com/fz5HIf7.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 3) Configure Departments (Ticket Visibility: Help Desk vs SysAdmins vs Networking)
**Path:** `Admin Panel -> Agents -> Departments`  
**Action taken:** Created department **SysAdmins**.

**Notes / Why:** Departments control ticket visibility and routing to the correct teams.

<p align="center">
<img src="https://i.imgur.com/db2Fdyv.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 4) Configure Teams
**Path:** `Admin Panel -> Agents -> Teams`  
**Action taken:** Created team **Online Banking** (pulled agents from different departments).

**Notes / Why:** Teams allow cross-department collaboration and shared queues.

<p align="center">
<img src="https://i.imgur.com/g7A5H9n.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 5) Allow anyone to create tickets (Registration settings)
**Path:** `Admin Panel -> Settings -> User Settings`  
**Action taken:** **UN-CHECKED** “Unregistered users can create tickets” → Enabled **Registration Required** (users must register/login to create tickets).

**Notes / Why:** Making sure to uncheck the box makes sure the server doesn't Force authenticated submissions, and improves accountability & control.

---


### 6) Configure Users (customers)
**Path:** `Agent Panel -> Users -> Add New`  
**Action taken:** Created users:  
- **Karen**  

**Notes / Why:** Create test or seed user accounts to validate registration, login, and ticket creation workflows.

<p align="center">
<img src="https://i.imgur.com/qifSDlQ.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 7) Configure SLA
**Path:** `Admin Panel -> Manage -> SLA`  
**Action taken:** Created SLAs:  
- **Sev-A** — Grace Period: 1 hour, Schedule: 24/7  
- **Sev-B** — Grace Period: 4 hours, Schedule: 24/7  
- **Sev-C** — Grace Period: 8 hours, Schedule: Business Hours

**Notes / Why:** Define response/resolve expectations and escalation rules.

<p align="center">
<img src="https://i.imgur.com/tzpW0Mv.png" alt="Prerequisite Files" width="80%"/>
</p>

---

### 8) Configure Help Topics (for the ticket submission form)
**Path:** `Admin Panel -> Manage -> Help Topics`  
**Action taken:** Created topics:  
- Business Critical Outage  
- Personal Computer Issues  
- Equipment Request  
- Password Reset  
- Other

**Notes / Why:** Help Topics present user-facing categories on the ticket form and can be used for routing and automations.

<p align="center">
<img src="https://i.imgur.com/oDueYaG.png" alt="Prerequisite Files" width="80%"/>
</p>


---

## Troubleshooting tips
- **User can’t create ticket:** Confirm **Registration Required** setting and user account status.  
- **Agent missing permissions:** Review Roles → Permissions and Department membership.  
- **SLA not applied:** Confirm ticket’s assigned help-topic/priority and SLA mapping rules.  
- **No notification/email:** Check Email settings (SMTP), test sending, and review mail logs.

here is the link to the next set of steps -> [osTicket: Ticket Lifecycle Examples](https://github.com/BerrickPhilbin/ticket-lifecycle)
