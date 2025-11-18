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

### 1) Configure Roles (for grouping permissions)
**Path:** `Admin Panel -> Agents -> Roles`  
**Action taken:** Created role **Supreme Admin**.

**Notes / Why:** Use roles to group and manage permission sets for agents.

**Imgur (step 1):**  
`https://imgur.com/your-image-here`  
`![Configure Roles](https://imgur.com/your-image-here)`

---

### 2) Configure Departments (Ticket Visibility: Help Desk vs SysAdmins vs Networking)
**Path:** `Admin Panel -> Agents -> Departments`  
**Action taken:** Created department **SysAdmins**.

**Notes / Why:** Departments control ticket visibility and routing to the correct teams.

**Imgur (step 2):**  
`https://imgur.com/your-image-here`  
`![Configure Departments](https://imgur.com/your-image-here)`

---

### 3) Configure Teams
**Path:** `Admin Panel -> Agents -> Teams`  
**Action taken:** Created team **Online Banking** (pulls agents from different departments).

**Notes / Why:** Teams allow cross-department collaboration and shared queues.

**Imgur (step 3):**  
`https://imgur.com/your-image-here`  
`![Configure Teams](https://imgur.com/your-image-here)`

---

### 4) Allow anyone to create tickets (Registration settings)
**Path:** `Admin Panel -> Settings -> User Settings`  
**Action taken:** **UN-CHECKED** “Unregistered users can create tickets” → Enabled **Registration Required** (users must register/login to create tickets).

**Notes / Why:** Forces authenticated submissions, improves accountability & control.

**Imgur (step 4):**  
`https://imgur.com/your-image-here`  
`![User Settings - Registration](https://imgur.com/your-image-here)`

---

### 5) Configure Agents (workers)
**Path:** `Admin Panel -> Agents -> Add New`  
**Action taken:** Created agents:  
- **Jane** — Department: SysAdmins  
- **John** — Department: Support

**Notes / Why:** Add agents and assign to departments for ticket handling and notifications.

**Imgur (step 5):**  
`https://imgur.com/your-image-here`  
`![Configure Agents](https://imgur.com/your-image-here)`

---

### 6) Configure Users (customers)
**Path:** `Agent Panel -> Users -> Add New`  
**Action taken:** Created users:  
- **Karen**  
- **Ken**

**Notes / Why:** Create test or seed user accounts to validate registration, login, and ticket creation workflows.

**Imgur (step 6):**  
`https://imgur.com/your-image-here`  
`![Configure Users](https://imgur.com/your-image-here)`

---

### 7) Configure SLA
**Path:** `Admin Panel -> Manage -> SLA`  
**Action taken:** Created SLAs:  
- **Sev-A** — Grace Period: 1 hour, Schedule: 24/7  
- **Sev-B** — Grace Period: 4 hours, Schedule: 24/7  
- **Sev-C** — Grace Period: 8 hours, Schedule: Business Hours

**Notes / Why:** Define response/resolve expectations and escalation rules.

**Imgur (step 7):**  
`https://imgur.com/your-image-here`  
`![Configure SLA](https://imgur.com/your-image-here)`

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

**Imgur (step 8):**  
`https://imgur.com/your-image-here`  
`![Configure Help Topics](https://imgur.com/your-image-here)`

---

## Troubleshooting tips
- **User can’t create ticket:** Confirm **Registration Required** setting and user account status.  
- **Agent missing permissions:** Review Roles → Permissions and Department membership.  
- **SLA not applied:** Confirm ticket’s assigned help-topic/priority and SLA mapping rules.  
- **No notification/email:** Check Email settings (SMTP), test sending, and review mail logs.

---

## Files & Notes
- Use `/images` for local screenshots, or host screenshots on Imgur and paste links into each `![alt](link)` slot above.  
- Convert any `https://imgur.com/your-image-here` placeholders to real Imgur direct-image links (for better embedding use `i.imgur.com/xxxxx.png` or the Markdown shown above).  
- Consider adding `.gitignore` to exclude local screenshot files if you prefer Imgur hosting.

---

## Next steps I can do for you
- Convert this README to HTML if you prefer the original HTML style.  
- Populate the README in your repo/canvas for you.  
- Create a `troubleshooting.md` or `CONTRIBUTING.md` file from the notes.

---

**Author / Maintainer:** _Your Name Here_  
**License:** MIT (suggested)  
