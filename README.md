<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" />
</p>

<h1>osTicket — Post-Install Configuration</h1>

This repository documents the **post-install configuration steps** I performed for osTicket (Windows 10 / IIS environment).

---

<h2>🧰 Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)  
- <b>Windows 10 Pro (21H2)
- Remote Desktop Protocol (RDP)
  
---

<h2>🎯 Post-Install Configuration Objectives</h2>

- Configure roles, departments, teams, agents, and users  
- Enforce registration requirements & user visibility  
- Configure SLAs, help topics, and basic security/hardening  
- Provide screenshot placeholders for documentation  

---

<h2>📝 Step 1: Configure Agents (Workers)</h2>

**Path:** `Admin Panel -> Agents -> Add New`  

**Action Taken:**  
Created agents:  
- **Jane** — Department: SysAdmins  
- **John** — Department: Support  

**Notes / Why:**  
Add agents and assign them to departments for ticket handling and notifications.

<p align="center">
<img src="https://i.imgur.com/M4MUWev.png" alt="Configure Agents" width="80%"/>
</p>

---

<h2>📝 Step 2: Configure Roles (Permissions Grouping)</h2>

**Path:** `Admin Panel -> Agents -> Roles`  

**Action Taken:**  
Created role **Supreme Admin**.

**Notes / Why:**  
Use roles to group and manage permission sets for agents.

<p align="center">
<img src="https://i.imgur.com/fz5HIf7.png" alt="Configure Roles" width="80%"/>
</p>

---

<h2>📝 Step 3: Configure Departments</h2>

**Path:** `Admin Panel -> Agents -> Departments`  

**Action Taken:**  
Created department **SysAdmins**.

**Notes / Why:**  
Departments control ticket visibility and route tickets to the correct teams (Help Desk vs SysAdmins vs Networking).

<p align="center">
<img src="https://i.imgur.com/0N5CrHo.png" alt="Configure Departments" width="80%"/>
</p>

---

<h2>📝 Step 4: Configure Teams</h2>

**Path:** `Admin Panel -> Agents -> Teams`  

**Action Taken:**  
Created team **Online Banking** (includes members from multiple departments).

**Notes / Why:**  
Teams allow cross-department collaboration and shared ticket queues.

<p align="center">
<img src="https://i.imgur.com/g7A5H9n.png" alt="Configure Teams" width="80%"/>
</p>

---

<h2>📝 Step 5: Set User Registration Requirements</h2>

**Path:** `Admin Panel -> Settings -> User Settings`  

**Action Taken:**  
**UN-CHECKED** “Unregistered users can create tickets” → Enabled **Registration Required**.

**Notes / Why:**  
Enforcing registration prevents anonymous submissions and improves accountability.

---

<h2>📝 Step 6: Configure Users (Customers)</h2>

**Path:** `Agent Panel -> Users -> Add New`  

**Action Taken:**  
Created user:  
- **Karen**

**Notes / Why:**  
Create test/seed user accounts to validate registration, login, and ticket creation workflows.

<p align="center">
<img src="https://i.imgur.com/qifSDlQ.png" alt="Configure Users" width="80%"/>
</p>

---

<h2>📝 Step 7: Configure SLAs</h2>

**Path:** `Admin Panel -> Manage -> SLA`  

**Action Taken:**  
Created SLAs:
- **Sev-A** — Grace: 1 hour, Schedule: 24/7  
- **Sev-B** — Grace: 4 hours, Schedule: 24/7  
- **Sev-C** — Grace: 8 hours, Schedule: Business Hours  

**Notes / Why:**  
SLAs define expected response/resolve windows and escalation policies.

<p align="center">
<img src="https://i.imgur.com/tzpW0Mv.png" alt="Configure SLA" width="80%"/>
</p>

---

<h2>📝 Step 8: Configure Help Topics</h2>

**Path:** `Admin Panel -> Manage -> Help Topics`  

**Action Taken:**  
Created topics:
- Business Critical Outage  
- Personal Computer Issues  
- Equipment Request  
- Password Reset  
- Other  

**Notes / Why:**  
Help Topics categorize incoming tickets and can trigger routing rules and automation.

<p align="center">
<img src="https://i.imgur.com/oDueYaG.png" alt="Help Topics" width="80%"/>
</p>

---

<h2>🛠 Troubleshooting Tips</h2>

- **User can’t create ticket:** Confirm "Registration Required" and user account status.  
- **Agent missing permissions:** Check Roles → Permissions and Department assignments.  
- **SLA not applied:** Verify help topic → priority → SLA rule mappings.  
- **Email/notification issues:** Review SMTP settings, test sending, and check mail logs.  

---

Here is the link to the next set of steps →  
👉 **[osTicket: Ticket Lifecycle Examples](https://github.com/BerrickPhilbin/ticket-lifecycle)**

