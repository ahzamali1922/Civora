# Civora — Features and Functional Modules

**Version:** 2.0  
**Status:** Planned

---

## 1. Authentication and User Management

### Features
- Citizen registration and login.
- Secure password hashing.
- Logout and token/session management.
- User profile management.
- Role-based access control.
- Account activation and deactivation.
- Password reset.

### User Roles
- Citizen
- Authority
- Administrator

## 2. Citizen Portal

### 2.1 Issue Reporting
Citizens can submit civic complaints through a structured form.

Information collected:
- Issue title.
- Issue description.
- Issue category.
- Supporting photographs.
- Address or location description.
- Latitude and longitude.
- Optional additional information.

### 2.2 My Complaints
Citizens can:
- View submitted complaints.
- View complaint details.
- Track complaint status.
- View assignment and progress updates.
- View resolution evidence.
- Reopen eligible complaints or request a review.

### 2.3 Public Issue Feed
- Browse public complaints.
- Filter by category.
- Filter by status.
- Search complaints.
- Sort by recent submissions.
- View complaint details.

## 3. AI-Powered Issue Classification

The ML subsystem assists in identifying the type of civic problem.

### 3.1 Image Classification
- Accept uploaded complaint images.
- Preprocess images.
- Run image classification.
- Predict the likely issue category.
- Return confidence information.

### 3.2 Text Classification
- Analyze complaint descriptions.
- Preprocess text.
- Generate text features.
- Predict the likely issue category.
- Return confidence information.

### 3.3 Prediction Combination
- Combine image and text predictions.
- Produce a suggested category.
- Track model confidence.
- Flag uncertain predictions for manual review.

**Important:** Classification should remain advisory. The system must support manual correction and record the final confirmed category.

## 4. Authority Management

Administrators can:
- Create authority departments.
- Update department information.
- Assign authority users to departments.
- Configure supported issue categories.
- Activate or deactivate departments.
- Monitor department performance.

Example departments:
- Roads and Infrastructure.
- Water Supply.
- Sanitation.
- Electricity and Street Lighting.
- Drainage and Sewerage.

## 5. Complaint Assignment

- Assign complaints to departments or authority users.
- Record assignment history.
- Allow authorities to accept or reject assignments.
- Require a reason for rejection.
- Reassign complaints when necessary.
- Track assignment timestamps.

The system should support both manual assignment and AI-assisted routing.

## 6. Complaint Resolution Workflow

### Planned Status Lifecycle

1. Submitted
2. Under Review
3. Assigned
4. In Progress
5. Resolved
6. Closed

Additional statuses:
- Rejected
- Reopened

### Authority Actions
- Review complaint details.
- Accept assignment.
- Start work.
- Add progress updates.
- Mark complaint as resolved.
- Upload resolution photographs.
- Provide resolution notes.

### Citizen Actions
- Track complaint progress.
- View authority updates.
- Confirm resolution where enabled.
- Request reopening or review according to platform rules.

## 7. Interactive Issue Map

- Display publicly visible complaints.
- Place markers using complaint coordinates.
- Use different marker styles for categories or statuses.
- Open complaint details from map markers.
- Filter map results.
- Support geographical clustering when complaint volume grows.

Technology: Leaflet with OpenStreetMap.

## 8. Notification System

Users can receive notifications for:
- Complaint submission confirmation.
- Complaint assignment.
- Assignment acceptance or rejection.
- Status changes.
- Resolution updates.
- Reopening or review outcomes.

Initial implementation may use in-app notifications. Email or push notifications can be added later.

## 9. Administrator Dashboard

- Total complaint count.
- Complaints by category.
- Complaints by status.
- Pending complaints.
- Resolved complaints.
- Department-wise performance.
- Complaint trends over time.
- User and authority management.

## 10. Authority Dashboard

- Assigned complaints.
- Pending assignments.
- In-progress complaints.
- Resolved complaints.
- Complaint details and location.
- Department-level statistics.
- Assignment history.

## 11. Search and Filtering

Supported filters:
- Category.
- Status.
- Date range.
- Department.
- Location.
- Assignment status.

Search should support complaint titles and descriptions.

## 12. System-Level Features

- REST API versioning.
- Centralized error handling.
- Request validation.
- Logging and monitoring.
- Image storage management.
- Background task processing.
- Automated testing.
- API documentation.

## 13. Feature Prioritization

| Priority | Features |
|---|---|
| P0 — Essential | Authentication, reporting, issue management, database, role permissions |
| P1 — Core | Classification, authority management, assignment, tracking |
| P2 — Important | Public map, notifications, dashboards, analytics |
| P3 — Future | Duplicate detection, prediction, chatbot, external integrations |

## 14. MVP Completion Criteria

The MVP is considered functional when:

- A citizen can register and log in.
- A citizen can submit a complaint with an image and location.
- The system can store and retrieve complaint data.
- The classification subsystem can suggest a category.
- An administrator can manage authorities.
- A complaint can be assigned to an authority.
- An authority can update complaint progress.
- A citizen can track the complaint.
- Important status changes are recorded.
- Unauthorized users cannot perform restricted actions.

---

**Document Owner:** Civora Development Team