# Event-Registration-Attendee-Management
Event Registration &amp; Attendee Management is a Salesforce-based solution designed to simplify event organization for institutions and businesses. This project enables organizers to create and manage event listings, register attendees, automate confirmation/reminder emails, and track attendance and engagement through dashboards and reports.

# Event Management System

## Problem Understanding & Industry Analysis
The core problem is that many organizations struggle to manage event registrations efficiently, leading to lost data, poor communication, and low attendee engagement. Most educational institutions, clubs, and businesses require a centralized system to handle registrations, automate notifications, and improve attendee experience.

## Requirement Gathering
Events must be created, scheduled, updated, and cancelled.

Attendees need to register for events with personal details (name, email, contact, etc.).

Organizers require automation for confirmation and reminders.

Attendance tracking and reports are necessary for insights.

Simple user interface for both admin and participants.

## Stakeholder Analysis
Event Organizers: Manage events, track registrations, analyze reports.

Attendees/Participants: Register for events, receive notifications, view schedules.

Admins: Oversee processes, manage users, troubleshoot issues.

## Business Process Mapping
Event creation → Registration opens → Attendee registers → Confirmation sent → Reminders sent → Event occurs → Attendance recorded → Feedback/metrics tracked.

Possible exceptions: Event rescheduling/cancellation, attendee unregistration.

## Industry-Specific Use Case Analysis
Educational Institutions: Manage workshops, seminars, student participation.

IT Companies: Employee training, hackathons, client events.

Professional Associations: Conferences, meetings, networking events.

## AppExchange Exploration
Review AppExchange apps for event management (Cvent, Blackthorn, etc.).

Analyze what features they offer: registration forms, automation, reporting, scalability.

Use insights for best practices and Salesforce-native enhancements.

# Phase 2: Org Setup & Configuration

This phase covers the Salesforce Developer Org setup and configuration for the **Event Registration & Attendee Management** project.

---

## 1. Salesforce Developer Org Setup
- Signed up for a **Salesforce Developer Edition** to build and test the event registration application.  
- Org Name: **Event Registration & Attendee Management**

---

## 2. Company Profile Configuration
- Entered basic organization information in **Setup > Company Information**.  
- Set the **project name** and provided a **contact email** for administrative tasks.

---

## 3. Profiles Creation
Created two custom profiles by cloning **Standard User**:

- **Event Organizer Profile**: Full access to event and attendee management functions.  
- **Event Attendee Profile**: Limited access, can only view and manage their own registrations.

---

## 4. Role Hierarchy Setup
Configured a three-level role hierarchy:

1. **Event Manager** → Top-level, access to all data.  
2. **Organizer** → Can access events they organize and associated attendees.  
3. **Attendee** → Can view only their own event registrations.  

---

## 5. User Accounts (Sample/Test)
Added sample users per role to validate permissions and feature access:
- **1 Event Manager**
- **1 Organizer**
- **1 Attendee**

Used **test email addresses** for demonstration.

---

## 6. Permission Sets (Optional Use)
- Created **permission sets** to grant additional access if required  
  (e.g., dashboard viewing for Organizers).

---

## 7. Org-Wide Defaults & Sharing Rules
- **Event Object** → Private (only owners and those above in role hierarchy can access).  
- **Attendee Object** → Controlled by Parent (Event), ensuring attendee records are protected.  

Sharing Rules:
- Configured rules for **Event Managers** and **Organizers** to enable collaborative event management.

---

## 8. Login Access Policies
- Used **default settings**.  
- No restrictions or IP range limitations applied (kept testing open for project members).

---

##  Summary of Phase 2 Steps

| Step                  | Action Taken                                                                 |
|-----------------------|-------------------------------------------------------------------------------|
| Developer Org Setup   | Created Salesforce Developer Org, named for the project                      |
| Company Profile       | Updated organization info and project name                                   |
| Profiles              | Created **Event Organizer** & **Attendee** profiles                          |
| Roles                 | Set up **Event Manager**, **Organizer**, and **Attendee** roles              |
| Sample Users          | Added one user per role for permissions testing                              |
| Permission Sets       | Created if needed for specialized access                                     |
| Org-Wide Defaults     | Event: **Private**, Attendee: **Controlled by Parent**; custom sharing rules |
| Login Access Policies | Kept default settings for development and testing                            |

---

 This configuration ensures **security**, **clarity in role responsibilities**, and prepares the org for **custom object creation** and **automation** tailored to event management.

