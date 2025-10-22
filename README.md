# ERP

# 🏢 Enterprise Resource Planning (ERP) Web Portal

A comprehensive, full-featured Enterprise Resource Planning (ERP) web application built with Flask and Firebase. This system provides complete employee lifecycle management, project tracking, financial operations, and business process automation for modern organizations.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.3.3-green.svg)
![License](https://img.shields.io/badge/License-Proprietary-red.svg)

---

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [User Roles & Permissions](#user-roles--permissions)
- [API Documentation](#api-documentation)
- [Deployment](#deployment)
- [Security Considerations](#security-considerations)
- [Usage Guide](#usage-guide)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This ERP portal is a production-ready enterprise management system designed to streamline organizational operations. It integrates human resources, project management, financial tracking, asset management, and employee evaluation into a unified platform. The system supports multi-role authentication with granular permissions, ensuring secure and efficient workflow management across departments.

### Built For
- Small to medium-sized enterprises
- Multi-department organizations
- Project-based companies
- Organizations requiring strict approval workflows
- Companies needing comprehensive employee management

---

## ✨ Key Features

### 🔐 Authentication & User Management
- **Multi-Role Authentication System**
  - Managing Director (MD)
  - Team Lead
  - HR (Human Resources)
  - Accounts Department
  - Procurement
  - Employee
- **Secure Authentication**
  - Password hashing with Werkzeug
  - Session-based authentication
  - Role-based access control (RBAC)
- **User Profile Management**
  - Complete employee information management
  - Document upload and storage
  - Profile customization
- **User Lifecycle Management**
  - User registration and onboarding
  - Soft delete functionality (restore capability)
  - Permanent deletion option
  - Created-by-admin tracking

### 📋 Request Management System

#### Permission Requests
- Submit permission requests for leaving office during work hours
- Multi-level approval workflow:
  1. Team Lead approval
  2. HR approval
  3. Director approval
- Track time-out and time-in
- Destination tracking
- Real-time status updates
- Digital signature collection

#### Leave Requests
- Comprehensive leave management
- Leave balance tracking
- Multi-level approval workflow:
  1. Reporting authority/Team Lead
  2. HR approval
  3. Director final approval
- Leave history and balance calculation
- Date range selection with time specification
- Reason documentation
- Digital signatures at each approval stage

#### Travel Requests
- Business travel request submission
- Journey details tracking
- Multi-destination support
- Purpose documentation
- Director approval required
- Budget tracking integration

#### Conveyance Claims
- Transportation expense claim submission
- Multiple claim entries per request
- Dual approval workflow:
  1. HR department review
  2. Accounts department approval
- "Seen" status tracking
- Claim detail documentation

#### Asset Requests (Indent Management)
- Comprehensive asset procurement workflow
- Multi-stage approval process:
  1. Indenter submission
  2. Team Lead justification
  3. Procurement vendor quotation
  4. Team Lead vendor selection
  5. Director/MD approval
  6. Accounts budget verification
  7. Procurement payment processing
  8. Final delivery tracking
- Features:
  - Reference file number tracking
  - Purchase type classification (Capital/Revenue)
  - Budget head allocation
  - GST applicability
  - Multiple item requests per indent
  - Vendor comparison (up to 3 vendors)
  - Discount tracking
  - Payment details management
  - Delivery confirmation
- PDF download capability

### 📊 Project Management

#### Organizational Projects
- Project creation and management
- Project details:
  - Project name and description
  - Start and end dates
  - Deadline tracking
  - Budget head allocation
  - Group assignment
  - Member management
- Team Lead project ownership
- Project-specific groups
- Task assignment within projects

#### Personal Projects & Tasks
- Individual project management
- Personal task creation and tracking
- Deadline management
- Task completion toggling
- Project-specific task organization
- Personal to-do lists

#### Task Assignment System
- Assign tasks to team members
- Task status tracking (Pending/Completed)
- Priority management
- Deadline tracking
- Assigned by/to tracking
- Completion timestamps
- Task count dashboard

### 👥 Team & Group Management

#### Teams
- Create and manage teams
- Team member assignment
- Team description and details
- Team-based access control
- Team Lead assignments

#### Project Groups
- Project-specific group creation
- Group types:
  - Development
  - Design
  - Marketing
  - Custom types
- Member assignment to groups
- Group deadline tracking
- Group descriptions

### 📢 Communication & Announcements
- Company-wide announcements
- Department-specific announcements
- Role-based targeting
- User-specific announcements
- Announcement priorities:
  - Low
  - Normal
  - High
  - Urgent
- Expiration date setting
- Active/inactive status
- Create, read, update, delete (CRUD) operations

### 👤 Employee Management

#### Comprehensive Employee Information
- **Personal Details**
  - Full name, email, DOB
  - Gender, marital status
  - Phone number and address
  - Emergency contacts
  - Father/Mother details
  - Spouse information

- **Professional Details**
  - Employee ID
  - Office branch
  - Designation
  - Date of joining
  - Probation period tracking
  - Confirmation date
  - Anniversary date
  - Employment status

- **Document Management**
  - Aadhaar card
  - PAN card
  - Resume/CV
  - Passport photo
  - 10th certificate
  - 12th certificate
  - Post-graduation certificate
  - PDC (Post-Dated Cheque)

- **Salary Information**
  - Actual gross salary
  - Probation salary
  - Confirmation salary
  - Detailed salary breakdown:
    - **Earnings:**
      - Basic salary
      - HRA (House Rent Allowance)
      - Conveyance allowance
      - Vehicle maintenance
      - Special allowance
      - Additional earnings
    - **Deductions:**
      - Provident Fund (PF)
      - ESI (Employee State Insurance)
      - Professional tax
      - Income tax
      - Advance deductions
      - Other deductions
      - Loss of pay

- **Leave Management**
  - Total leaves allocated
  - Leaves availed
  - Balance leaves
  - Loss of Pay (LOP) days tracking
  - Total working days
  - Net days payable (NDP)

- **Academic Records**
  - Post-graduation marks
  - Educational certificates

- **Financial Details**
  - Account number
  - Bank details
  - Salary structure management

### 📈 Performance Evaluation System

#### Multi-Page Evaluation Form
A comprehensive 6-page evaluation system:

**Page 1: Employee Basic Information**
- Name, position, contact details
- Office branch, employee ID
- Employment status (Internship/Probation/Confirmation)
- Status duration
- Current salary

**Page 2: Self Evaluation (Employee)**
13 evaluation criteria with scores and comments:
- Attendance & punctuality
- Discipline
- Knowledge & skills
- Quality of work
- Teamwork & cooperation
- Work consistency
- Thinking process
- Communication skills
- Initiative
- Motivation
- Creativity
- Honesty & integrity
- Overall rating

**Page 3: Team Lead Evaluation**
Same 13 criteria from Team Lead perspective

**Page 4: HR Evaluation**
7 HR-specific criteria:
- Commitment to work
- Work attitude
- Team orientation
- Integrity & honesty
- Productivity
- Punctuality
- Physical disposition
- Overall HR assessment

**Page 5: Director Evaluation**
- Stability assessment
- Additional comments

**Page 6: Managing Director Final Decision**
- Further action (Hold/Next Round)
- Suitability decision (Yes/No)
- Project assignment
- Area assignment (SSEV/SSEV NATURO FARMS)
- Final comments

#### Evaluation Features
- Draft saving capability
- Multi-role workflow
- Digital signatures
- Date tracking
- Status progression tracking
- Evaluation report viewing
- Complete audit trail

### 📅 Attendance Management
- **Firebase Integration**
  - Real-time attendance tracking
  - Google Drive integration
  - Attendance data import from Firebase
- **Attendance Status**
  - Present
  - Absent
  - Late
  - Half Day
- **Features**
  - Check-in/Check-out time tracking
  - Date-wise attendance
  - Attendance reports
  - PDF report generation
  - Remarks/notes capability
  - Unique constraint (one record per user per day)

### 🎊 Holiday Management
- Add company holidays
- Holiday name and date
- Holiday calendar
- Created by tracking
- Delete holidays
- View all holidays

### 🏭 Vendor Management
- Vendor registration
- Vendor details:
  - Name and address
  - Contact number
  - Email
  - GST number
  - Creation tracking
- CRUD operations
- Integration with asset requests

### 🔧 Role & Permission Management
- **Default Roles**
  - Admin
  - CEO
  - CTO
  - CFO
  - Director
  - Manager
  - Employee
  - Accounts
  - Finance
  - Procurement

- **Features**
  - Custom role creation
  - Granular permissions
  - Role-based access control
  - Permission templates
  - Multiple roles per user
  - Role deletion (with safeguards)

### 📊 Dashboard & Analytics

#### Multi-Dashboard Support
- **Managing Director Dashboard**
  - Complete system overview
  - All pending approvals
  - Company-wide analytics
  
- **Team Lead Dashboard**
  - Team management
  - Task assignments
  - Team member requests
  - Project overview
  
- **HR Dashboard**
  - Employee management
  - Leave requests
  - Permission requests
  - Conveyance claims
  - Employee information access
  
- **Accounts Dashboard**
  - Conveyance claims
  - Asset request budget verification
  - Financial approvals
  
- **Employee Dashboard**
  - Personal requests
  - Assigned tasks
  - Personal projects
  - Announcements

#### Dashboard Analytics
- Task counts (pending/completed)
- Project counts
- Request status summaries
- Quick action buttons
- Real-time notifications

### 📄 Reporting & Document Generation
- **PDF Report Generation**
  - ReportLab integration
  - Attendance reports
  - Employee reports
  - Asset request PDFs
  - Custom report templates
  
- **Export Capabilities**
  - PDF downloads
  - Data export functionality
  - Document management

### 🔄 Database Management
- **Migration Tools**
  - Built-in database migration endpoints
  - Schema updates
  - Data integrity checks
  - Migration status tracking
  
- **Data Integrity**
  - Foreign key relationships
  - Cascade delete options
  - Unique constraints
  - Soft delete implementation

### 🔔 Notification System
- Real-time status updates
- Request approval notifications
- Task assignment alerts
- Announcement notifications

---

## 🛠️ Technology Stack

### Backend Technologies
- **Flask 2.3.3** - Python web framework
- **SQLAlchemy** - ORM for database management
- **Flask-SQLAlchemy 3.1.1** - Flask integration for SQLAlchemy
- **SQLite** - Local database storage (users.db)
- **Firebase Admin SDK** - Cloud database and Firestore integration
- **Werkzeug 2.3.7** - Security utilities (password hashing)

### Frontend Technologies
- **HTML5** - Semantic markup
- **CSS3** - Modern styling
- **JavaScript** - Client-side interactivity
- **Responsive Design** - Mobile-friendly interface

### Integration & APIs
- **Google APIs**
  - Google Drive API
  - Google Sheets API
  - Google OAuth 2.0
- **Firebase Firestore** - Cloud database
- **Google API Python Client** - API integration

### Data Processing & Reporting
- **Pandas** - Data manipulation and analysis
- **ReportLab** - PDF generation (reports, attendance)
- **WeasyPrint** - HTML to PDF conversion
- **PyTZ** - Timezone management (Asia/Kolkata)

### File Handling
- **Werkzeug FileStorage** - Secure file uploads
- **Secure Filename** - File name sanitization
- **Multiple format support** - PDF, DOC, DOCX, images

### Development Tools
- **Python 3.8+** - Programming language
- **pip** - Package management
- **Git** - Version control
- **Virtual Environment** - Dependency isolation

### Deployment
- **Passenger WSGI** - Production deployment
- **wsgi.py** - WSGI application entry point
- **passenger_wsgi.py** - Passenger configuration

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Git (for version control)
- Firebase project with Firestore enabled
- Google Cloud project (for API access)

### Step-by-Step Setup

#### 1. Clone the Repository
   ```bash
   git clone https://github.com/bhargavikorimi/ERP-Web-Project.git
   cd ERP-Web-Project
   ```

#### 2. Create Virtual Environment
   ```bash
# Create virtual environment
   python -m venv venv
   
# Activate virtual environment
# On Windows:
   venv\Scripts\activate
   
# On macOS/Linux:
   source venv/bin/activate
   ```

#### 3. Install Dependencies
   ```bash
   pip install -r requirements.txt
   ```

#### 4. Firebase Configuration
1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Generate a service account key:
   - Go to Project Settings → Service Accounts
   - Click "Generate New Private Key"
   - Save the JSON file as `firebase-service-account.json` in the project root

#### 5. Google Drive API Setup (Optional)
If using Google Drive integration for attendance:
1. Enable Google Drive API in Google Cloud Console
2. Create OAuth 2.0 credentials
3. Download credentials and configure in the application

#### 6. Create Required Directories
   ```bash
   mkdir uploads
   ```

#### 7. Configure Application
Edit `app.py` and update:
```python
# Change the secret key for production
app.secret_key = 'your-super-secret-key-here'

# Verify database path
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///users.db'

# Verify upload folder
UPLOAD_FOLDER = 'uploads'
```

#### 8. Initialize Database
   ```bash
   python app.py
   ```
The database (`users.db`) will be automatically created with all necessary tables on first run.

#### 9. Run the Application
   ```bash
   python app.py
   ```
   The application will be available at `http://localhost:5000`

#### 10. Create First Admin User
1. Navigate to `http://localhost:5000/register`
2. Register a new user
3. Access the database to assign admin roles:
```bash
# Using SQLite command line
sqlite3 users.db

# Assign roles (example)
INSERT INTO user_roles (user_id, role_id) VALUES (1, 1);
```

---

## 📂 Project Structure

```
ERP-Web-Project/
│
├── app.py                          # Main application file (6000+ lines)
├── wsgi.py                         # WSGI entry point
├── passenger_wsgi.py               # Passenger WSGI configuration
├── requirements.txt                # Python dependencies
├── users.db                        # SQLite database (auto-generated)
├── firebase-service-account.json   # Firebase credentials (gitignored)
│
├── static/                         # Static files
│   ├── images/                     # Image assets
│   │   ├── logo.png
│   │   ├── img1.png
│   │   ├── img2.jpeg
│   │   ├── img3.jpeg
│   │   ├── img4.jpeg
│   │   └── img5.png
│   └── videos/                     # Video backgrounds (14 MP4 files)
│
├── templates/                      # HTML templates
│   ├── index.html                  # Landing page
│   ├── login.html                  # Login page
│   ├── register.html               # Registration page
│   ├── dashboard.html              # Main dashboard
│   ├── multi_dashboard.html        # Multi-role dashboard
│   ├── evaluation_start.html       # Evaluation start page
│   └── evaluation_evaluate.html    # Evaluation form
│
├── uploads/                        # User uploaded files (gitignored)
│   └── [employee documents]        # PDFs, images, certificates
│
├── github/                         # GitHub-specific files
│   ├── app.py
│   ├── requirements.txt
│   ├── README.md
│   └── [static/templates mirrors]
│
└── __pycache__/                    # Python cache (gitignored)
```

---

## 🗄️ Database Schema

### Core Tables

#### User Table
```python
- id (Primary Key)
- name
- username
- email (Unique)
- password (Hashed)
- created_by_admin (Boolean)
- pf_no (PF Number)
- is_deleted (Soft delete flag)
- roles (Many-to-Many with Role)
```

#### Role Table
```python
- id (Primary Key)
- name (Unique)
```

#### User-Roles Association Table
```python
- user_id (Foreign Key)
- role_id (Foreign Key)
```

### Request Tables

#### LeaveRequest
```python
- id, user_id, team_lead_id
- spv_name, department, emp_no, contact_details
- applicant_name, total_leaves, leave_availed, balance_leaves
- from_date, from_time, to_date, to_time
- reason, status
- applicant_sign, applicant_sign_date
- reporting_authority_sign, reporting_authority_date
- hr_sign, hr_date
- director_sign, director_date
- remarks
```

#### PermissionRequest
```python
- id, user_id, team_lead_id
- spv_name, date, applicant_name, reason
- time_out, time_in, going_to
- applicant_sign, approver_sign
- team_lead_sign, hr_sign, director_sign
- status
```

#### TravelRequest
```python
- id, user_id, company, date
- purpose, journey_details (JSON)
- applicant_sign, director_sign
- status
```

#### ConveyanceRequest
```python
- id, user_id
- claim_details (JSON)
- status_hr, status_accounts
- request_date
```

#### AssetRequest
```python
- id, indenter_id, indenter_name
- office_project_type, project_id, team_lead_id
- reference_file_no, purchase_type
- budget_head, nature_of_expenditure, gst_applicable
- item_details (JSON)
- request_date, justification
- procurement_items (JSON)
- finalized_vendor, approval_procurement
- director approvals (pi, pd, chairman)
- MD approvals
- accounts_approval, accounts_comments
- budget_allocation, budget_utilized, available_balance
- procurement payment details
- final_delivery_status, handed_over_to
- discount_amount, status
```

### Project Tables

#### Project
```python
- id, project_name, group_name
- members, start_date, end_date, deadline
- budget_head, created_by
```

#### Team
```python
- id, name (Unique), description
- created_at
- members (Many-to-Many with User)
```

#### Group
```python
- id, name, group_type, description
- project_id, deadline, created_at
- members (Many-to-Many with User)
```

#### Task
```python
- id, task_name
- assigned_by_id, assigned_to_id
- status, created_at, completed_at
```

#### ProjectTask
```python
- id, task_name, deadline
- is_completed, project_id, user_id
- created_at, completed_at
```

#### PersonalProject & PersonalTask
```python
PersonalProject: id, name, user_id
PersonalTask: id, name, description, deadline, completed, project_id
```

### HR & Employee Tables

#### EmployeeInfo
```python
# Personal Details
- id, user_id, full_name, email, dob, gender
- father_name, father_contact
- mother_name, mother_contact
- emergency_contact_name, emergency_phone_number
- spouse_name, spouse_contact_number
- phone_no, address, marital_status

# Professional Details
- office_branch, employee_id, designation
- probation_from, probation_to
- date_of_joining, confirmation_date, date_of_anniversary
- probation_salary, confirmation_salary

# Documents
- pdc, aadhaar_card, pan_card, resume, passport_photo
- tenth_certificate, twelfth_certificate
- post_graduation_certificate, post_graduation_marks

# Financial Details
- account_number, actual_gross_salary
# Earnings
- basic, hra, conveyance, vehicle_maintenance
- special_allowance, add_others
- earnings_basic, earnings_hra, earnings_conveyance
- earnings_vehicle_maintenance, earnings_special_allowance
- earnings_add_others
# Deductions
- provident_fund, esi, professional_tax
- income_tax, advance, other_deductions, loss_of_pay

# Leave & Attendance
- leave_availed, balance_leaves, total_leaves
- no_of_lop_days, total_days, ndp
- is_deleted
```

#### Attendance
```python
- id, user_id, date
- check_in_time, check_out_time
- status, remarks, created_at
- Unique constraint: (user_id, date)
```

#### Holiday
```python
- id, name, date
- created_by, created_at
```

### Evaluation Tables

#### EvaluationReport
```python
- id, employee_id, team_lead_id, status
- created_at, updated_at
# Employee Details
- name, position, contact_number, email_id
- office_branch, employee_id_str
- employment_status, status_duration, salary
```

#### EvaluationResponse
```python
- id, evaluation_report_id, evaluator_id
- evaluator_role, page_number
# Self Evaluation (13 criteria)
- attendance_score, attendance_comments
- discipline_score, discipline_comments
- [... 11 more criteria]
# HR Evaluation (7 criteria)
- commitment_work_score, commitment_work_comments
- [... 6 more criteria]
# Director/MD Evaluation
- stability_score, stability_comments
- further_action_hold, further_action_next_round
- suitable_yes, suitable_no
- project_assignment, area_assignment
# Signatures
- signature, evaluator_name, evaluation_date
```

### Other Tables

#### Announcement
```python
- id, title, content, author_id
- created_at, updated_at, is_active
- priority, target_roles (JSON), target_users (JSON)
- expires_at
```

#### Vendor
```python
- id, name, address
- contact_no, email, gst_number
- created_at, created_by
```

#### RolePermissions
```python
- id, role_name
- permissions (JSON/Text)
```

---

## 👥 User Roles & Permissions

### Role Hierarchy

#### 1. Managing Director (MD)
**Highest Authority**
- Complete system access
- Final approval for all requests
- View all employee data
- Manage all projects
- Access all dashboards
- Perform evaluations (Page 6)
- Approve/reject asset requests
- View financial data
- Manage users and roles

**Permissions:**
- ✅ All CRUD operations
- ✅ Final approval authority
- ✅ Override capabilities
- ✅ System configuration
- ✅ View all analytics

#### 2. Director
**Senior Management**
- Approve leave requests
- Approve permission requests
- Approve travel requests
- Review asset requests
- Perform evaluations (Page 5)
- View department analytics
- Manage projects

**Permissions:**
- ✅ Request approvals (final stage)
- ✅ View employee information
- ✅ Project oversight
- ✅ Department analytics
- ✅ Evaluation access

#### 3. Team Lead
**Middle Management**
- First-level approval for team requests
- Assign tasks to team members
- Manage team projects
- Create and manage groups
- Submit asset requests
- Justify procurement needs
- Perform team evaluations (Page 3)

**Permissions:**
- ✅ Team member management
- ✅ Task assignment
- ✅ Project creation
- ✅ Request approval (first level)
- ✅ Team analytics
- ✅ Evaluation of team members

#### 4. HR (Human Resources)
**Employee Management**
- Second-level approval for leave/permission
- Manage employee information
- View and update employee records
- Handle conveyance claims
- Access attendance records
- Perform HR evaluations (Page 4)
- Manage holidays

**Permissions:**
- ✅ Employee data CRUD
- ✅ Leave/permission approval
- ✅ Attendance management
- ✅ Document verification
- ✅ HR evaluations
- ✅ Conveyance review

#### 5. Accounts Department
**Financial Management**
- Review conveyance claims (final approval)
- Verify asset request budgets
- Manage budget allocation
- Process payments
- Financial reporting

**Permissions:**
- ✅ Conveyance approval
- ✅ Budget verification
- ✅ Payment processing
- ✅ Financial data access
- ✅ Asset request budget check

#### 6. Procurement
**Purchase Management**
- Handle asset requests (procurement stage)
- Vendor quotation entry
- Vendor comparison
- Payment details entry

**Permissions:**
- ✅ Asset request updates
- ✅ Vendor management
- ✅ Quotation entry
- ✅ Delivery confirmation

#### 7. Employee
**Standard User**
- Submit requests (leave, permission, travel, conveyance, assets)
- View personal dashboard
- Manage personal projects
- Complete assigned tasks
- View announcements
- Perform self-evaluation (Page 2)
- Update personal information

**Permissions:**
- ✅ Submit requests
- ✅ View own data
- ✅ Personal project management
- ✅ Task completion
- ✅ Self-evaluation

### Permission Matrix

| Feature | Employee | Team Lead | HR | Accounts | Procurement | Director | MD |
|---------|----------|-----------|----|-----------|--------------|-----------|----|
| Submit Requests | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Approve Requests (L1) | ❌ | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ |
| Approve Requests (L2) | ❌ | ❌ | ✅ | ✅ | ❌ | ✅ | ✅ |
| Final Approval | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |
| Manage Employees | ❌ | Partial | ✅ | Partial | ❌ | ✅ | ✅ |
| Create Projects | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| Assign Tasks | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| View Analytics | Own | Team | Full | Financial | ❌ | Full | Full |
| Manage Vendors | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ |
| Budget Approval | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ✅ |
| Evaluations | Self | Team | HR | ❌ | ❌ | Director | Final |

---

## 🔌 API Documentation

### Authentication APIs

#### POST `/register`
Register a new user
```json
Request:
{
  "name": "John Doe",
  "username": "johndoe",
  "email": "john@example.com",
  "password": "securepassword"
}
```

#### POST `/login`
User login
```json
Request:
{
  "email": "john@example.com",
  "password": "securepassword"
}
```

#### GET `/logout`
Logout current user

### User Management APIs

#### POST `/api/add_user`
Add new user (Admin)

#### GET `/api/users`
Get all active users

#### GET `/api/get_user`
Get current user info

#### POST `/api/update_user`
Update user details

#### POST `/api/delete_user`
Soft delete user

#### GET `/api/deleted_users`
Get soft-deleted users

#### POST `/api/restore_user`
Restore deleted user

#### POST `/api/permanent_delete_user`
Permanently delete user

#### GET `/api/team_leads`
Get all team leads

#### POST `/api/change_password`
Change user password

### Request Management APIs

#### Permission Requests
- `POST /api/submit_permission_request` - Submit new permission request
- `GET /api/permission_request/<id>` - Get permission request details
- `POST /api/approve_permission_request_teamlead/<id>` - Team Lead approval
- `POST /api/approve_permission_request_hr/<id>` - HR approval
- `POST /api/approve_permission_request_director/<id>` - Director approval

#### Leave Requests
- `POST /api/submit_leave_request` - Submit leave request
- `GET /api/leave_request/<id>` - Get leave request details
- `GET /api/user_leave_info` - Get user leave balance
- `POST /api/approve_leave_request_teamlead/<id>` - Team Lead approval
- `POST /api/approve_leave_request_hr/<id>` - HR approval
- `POST /api/approve_leave_request_director/<id>` - Director approval

#### Travel Requests
- `POST /api/submit_travel_request` - Submit travel request
- `GET /api/travel_request/<id>` - Get travel request details
- `POST /api/approve_travel_request_director/<id>` - Director approval

#### Conveyance Claims
- `POST /api/submit_conveyance_claim` - Submit conveyance claim
- `GET /api/conveyance_request/<id>` - Get claim details
- `POST /api/mark_conveyance_claim_seen/<id>` - Mark as seen
- `GET /api/hr/conveyance_requests` - HR pending requests
- `GET /api/hr/seen_conveyance_requests` - HR seen requests
- `GET /api/accounts/conveyance_requests` - Accounts pending requests
- `GET /api/accounts/seen_conveyance_requests` - Accounts seen requests

#### Asset Requests
- `POST /api/asset_requests` - Submit asset request
- `GET /api/asset_requests` - Get asset requests (filtered by role)
- `GET /api/asset_requests/<id>` - Get specific request
- `POST /api/asset_requests/<id>/update` - Update asset request
- `POST /api/asset_requests/<id>/reject` - Reject request
- `GET /api/asset_requests/<id>/download` - Download PDF
- `GET /api/my_pending_indents` - User's pending requests
- `GET /api/my_approved_requests` - User's approved requests
- `GET /api/asset_form_options` - Get form dropdown options

### Aggregated Request APIs
- `GET /api/my_requests` - User's all requests
- `GET /api/teamlead/requests` - Team Lead pending requests
- `GET /api/teamlead/all_requests` - Team Lead all requests
- `GET /api/hr/requests` - HR pending requests
- `GET /api/hr/finalized_requests` - HR finalized requests
- `GET /api/hr/finalized_all_requests` - HR all finalized requests
- `GET /api/director/requests` - Director pending requests
- `GET /api/director/all_requests` - Director all requests

### Project Management APIs

#### Projects
- `POST /api/add_project` - Create project
- `GET /api/projects` - Get all projects
- `GET /api/my_projects` - User's projects
- `DELETE /api/delete_project/<id>` - Delete project
- `GET /project/<id>` - View project details
- `GET /api/user/projects` - User's personal projects
- `POST /api/user/projects` - Create personal project

#### Teams
- `GET /api/teams` - Get all teams
- `POST /api/teams` - Create team
- `PUT /api/teams/<id>` - Update team
- `DELETE /api/teams/<id>` - Delete team

#### Groups
- `GET /api/groups/<project_id>` - Get project groups
- `POST /api/groups` - Create group
- `GET /api/groups/<id>` - Get group details
- `PUT /api/groups/<id>` - Update group
- `DELETE /api/groups/<id>` - Delete group

### Task Management APIs

#### Organizational Tasks
- `POST /api/assign_task` - Assign task
- `GET /api/my_tasks` - User's assigned tasks
- `GET /api/assigned_tasks` - Tasks assigned by user
- `GET /api/my_assigned_tasks` - Tasks assigned to user
- `POST /api/complete_task/<id>` - Mark task complete
- `GET /api/active_users_for_tasks` - Get users for task assignment

#### Personal Project Tasks
- `GET /api/project/<project_id>/tasks` - Get project tasks
- `POST /api/project/<project_id>/tasks` - Add task
- `POST /api/task/<id>/toggle` - Toggle task completion
- `GET /api/project/<project_id>/personal_tasks` - Get personal project tasks
- `POST /api/project/<project_id>/add_personal_task` - Add personal task
- `POST /api/personal_project_task/<id>/toggle` - Toggle personal task

### Employee Management APIs

#### Employee Information
- `POST /api/add_employee_info` - Add employee information
- `GET /api/get_all_employee_info` - Get all employees
- `GET /api/get_employee_info/<id>` - Get specific employee
- `POST /api/update_employee_info` - Update employee info
- `POST /api/update_employee_designation/<id>` - Update designation
- `DELETE /api/delete_employee_info/<id>` - Delete employee info
- `POST /api/get_employee_report_data` - Get employee report data

#### Salary Management
- `GET /api/get_employee_salary_info/<id>` - Get salary details
- `POST /api/update_employee_salary` - Update salary

### Attendance APIs
- `GET /api/attendance/today` - Today's attendance
- `GET /api/attendance/both/<date>` - Attendance for specific date
- `POST /api/get_attendance_from_firebase` - Import from Firebase
- `GET /api/download_attendance_report` - Download PDF report

### Evaluation APIs
- `GET /evaluation/start` - Start evaluation page
- `GET /evaluation/evaluate` - Evaluation form page
- `GET /api/evaluation/user_info/<user_id>` - Get user info for evaluation
- `GET /api/evaluation/team_leads` - Get team leads
- `POST /api/evaluation/submit` - Submit evaluation report
- `GET /api/evaluation/reports` - Get evaluation reports
- `GET /api/evaluation/report/<id>` - Get specific report
- `POST /api/evaluation/submit_response` - Submit evaluation response

### Announcement APIs
- `GET /api/announcements` - Get announcements (filtered)
- `GET /api/announcements/all` - Get all announcements
- `POST /api/announcements` - Create announcement
- `PUT /api/announcements/<id>` - Update announcement
- `DELETE /api/announcements/<id>` - Delete announcement

### Holiday APIs
- `GET /api/holidays` - Get all holidays
- `POST /api/holidays` - Add holiday
- `DELETE /api/holidays/<id>` - Delete holiday

### Vendor APIs
- `GET /api/vendors` - Get all vendors
- `POST /api/vendors` - Create vendor
- `GET /api/vendors/<id>` - Get vendor details
- `PUT /api/vendors/<id>` - Update vendor

### Role & Permission APIs
- `POST /api/add_role` - Create role
- `GET /api/roles` - Get all roles
- `GET /api/get_role_permissions/<role_name>` - Get role permissions
- `DELETE /api/delete_role/<role_name>` - Delete role
- `POST /api/save_role_permissions` - Save role permissions
- `GET /api/user_modules` - Get user modules/permissions
- `GET /api/user/roles` - Get current user roles

### Dashboard APIs
- `GET /api/dashboard/task_counts` - Get task counts
- `GET /api/dashboard/project_counts` - Get project counts
- `GET /api/user_permissions_count` - Get user permission count

### Utility APIs
- `GET /uploads/<filename>` - Serve uploaded file
- `POST /api/migrate_database` - Database migration
- `GET /api/migration_status` - Migration status
- `GET /api/debug_all_indents` - Debug asset requests
- `GET /api/debug_user_info` - Debug user info
- `GET /test_md_data` - Test MD data

---

## 🚀 Deployment

### Development Deployment
```bash
# Activate virtual environment
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Run development server
python app.py
```
Access at `http://localhost:5000`

### Production Deployment with Passenger WSGI

#### Prerequisites
- Shared hosting or VPS with Passenger support
- Python 3.8+ installed
- SSH access

#### Deployment Steps

1. **Upload Files**
```bash
# Using SCP
scp -r * user@your-server.com:/path/to/app/

# Or using FTP/SFTP client
```

2. **Set Up Virtual Environment on Server**
```bash
ssh user@your-server.com
cd /path/to/app/
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

3. **Configure Passenger**
Ensure `passenger_wsgi.py` is configured:
```python
import sys
import os

INTERP = os.path.join(os.environ['HOME'], 'path', 'to', 'venv', 'bin', 'python3')
if sys.executable != INTERP:
    os.execl(INTERP, INTERP, *sys.argv)

sys.path.append(os.getcwd())

from app import app as application
```

4. **Set Environment Variables**
Create `.htaccess` or configure server:
```apache
SetEnv GOOGLE_APPLICATION_CREDENTIALS /path/to/firebase-service-account.json
SetEnv SECRET_KEY your-production-secret-key
```

5. **File Permissions**
```bash
chmod 644 app.py
chmod 644 wsgi.py
chmod 755 uploads/
```

6. **Restart Server**
```bash
# Passenger-specific
touch tmp/restart.txt

# Or restart web server
sudo systemctl restart apache2  # or nginx
```

### Docker Deployment (Optional)

Create `Dockerfile`:
```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["python", "app.py"]
```

Build and run:
```bash
docker build -t erp-portal .
docker run -p 5000:5000 -v ./uploads:/app/uploads erp-portal
```

### Environment Configuration

#### Production Environment Variables
```bash
export SECRET_KEY="your-super-secret-production-key"
export FLASK_ENV="production"
export DATABASE_URI="sqlite:///users.db"
export GOOGLE_APPLICATION_CREDENTIALS="firebase-service-account.json"
```

#### Configuration Checklist
- [ ] Change `app.secret_key` from default
- [ ] Set `FLASK_ENV=production`
- [ ] Configure Firebase credentials
- [ ] Set up SSL/HTTPS
- [ ] Configure file upload limits
- [ ] Set up backup strategy
- [ ] Configure logging
- [ ] Set up monitoring
- [ ] Enable CORS if needed
- [ ] Configure rate limiting

### Database Backup
```bash
# Backup SQLite database
cp users.db users_backup_$(date +%Y%m%d).db

# Scheduled backup (crontab)
0 2 * * * cp /path/to/users.db /path/to/backups/users_$(date +\%Y\%m\%d).db
```

---

## 🔒 Security Considerations

### Critical Security Measures

#### 1. Secret Key Management
```python
# ❌ BAD - Default key in production
app.secret_key = 'supersecretkey'

# ✅ GOOD - Use environment variable
import os
app.secret_key = os.environ.get('SECRET_KEY') or os.urandom(24)
```

#### 2. Firebase Credentials
```bash
# Add to .gitignore
echo "firebase-service-account.json" >> .gitignore

# Use environment variable for path
export GOOGLE_APPLICATION_CREDENTIALS="/secure/path/firebase-service-account.json"
```

#### 3. Password Security
- ✅ Passwords are hashed using Werkzeug's `generate_password_hash`
- ✅ Use `check_password_hash` for verification
- ✅ Never store plain-text passwords

#### 4. File Upload Security
```python
# Implemented safeguards:
ALLOWED_EXTENSIONS = {'txt', 'pdf', 'png', 'jpg', 'jpeg', 'gif', 'doc', 'docx'}
MAX_CONTENT_LENGTH = 16 * 1024 * 1024  # 16MB limit
secure_filename()  # Sanitize filenames
```

#### 5. SQL Injection Prevention
- ✅ Using SQLAlchemy ORM (parameterized queries)
- ✅ No raw SQL with user input

#### 6. Session Security
```python
# Add these configurations:
app.config['SESSION_COOKIE_SECURE'] = True  # HTTPS only
app.config['SESSION_COOKIE_HTTPONLY'] = True  # No JavaScript access
app.config['SESSION_COOKIE_SAMESITE'] = 'Lax'  # CSRF protection
```

#### 7. HTTPS/SSL
```python
# Force HTTPS in production
from flask_talisman import Talisman
Talisman(app, content_security_policy=None)
```

### Security Checklist

#### Before Production Deployment
- [ ] Change default secret key
- [ ] Enable HTTPS/SSL
- [ ] Secure Firebase credentials
- [ ] Add CSRF protection
- [ ] Implement rate limiting
- [ ] Set secure session cookies
- [ ] Configure CORS properly
- [ ] Add input validation
- [ ] Implement logging
- [ ] Set up monitoring
- [ ] Regular security updates
- [ ] Database access controls
- [ ] File upload restrictions
- [ ] Error message sanitization
- [ ] Backup strategy

#### Recommended Additional Security
```bash
pip install flask-talisman  # HTTPS enforcement
pip install flask-limiter   # Rate limiting
pip install flask-wtf       # CSRF protection
```

### File Upload Restrictions
```python
# Validate file types
def allowed_file(filename):
    return '.' in filename and \
           filename.rsplit('.', 1)[1].lower() in ALLOWED_EXTENSIONS

# Scan for malware (recommended)
# pip install clamd
import clamd
cd = clamd.ClamdUnixSocket()
```

### Access Control
- ✅ Role-based access control (RBAC)
- ✅ Session-based authentication
- ✅ @login_required decorators
- ✅ Role verification on sensitive operations

### Data Protection
```python
# Add to production:
- Regular database backups
- Encrypt sensitive data at rest
- Secure file storage
- Audit logging
- Data retention policies
```

---

## 📖 Usage Guide

### Getting Started

#### 1. First Time Setup
1. **Access the Application**
   - Navigate to `http://localhost:5000` (development) or your production URL
   
2. **Register First Admin**
   - Click "Register" on the landing page
   - Fill in user details
   - Complete registration

3. **Assign Admin Role**
   - Access database directly (first time only):
   ```bash
   sqlite3 users.db
   SELECT * FROM user;
   SELECT * FROM role;
   INSERT INTO user_roles (user_id, role_id) VALUES (1, 1);
   ```

4. **Login**
   - Use registered credentials
   - Access dashboard

### Common Workflows

#### For Employees

##### Submitting a Leave Request
1. Login to dashboard
2. Navigate to "Leave Requests"
3. Click "Submit Leave Request"
4. Fill in details:
   - From date/time
   - To date/time
   - Reason for leave
   - Leave balance will show automatically
5. Add digital signature
6. Submit
7. Track status in "My Requests"

##### Submitting a Permission Request
1. Go to "Permission Requests"
2. Click "New Permission"
3. Enter:
   - Date
   - Time out/Time in
   - Destination
   - Reason
4. Submit for approval

##### Managing Personal Tasks
1. Access "Multi Dashboard"
2. Create personal project
3. Add tasks to project
4. Set deadlines
5. Mark tasks complete

#### For Team Leads

##### Approving Team Requests
1. Dashboard shows pending approvals
2. Click on request to review
3. View employee details and request info
4. Approve or reject with comments
5. Digital signature required

##### Assigning Tasks
1. Go to "Task Management"
2. Click "Assign Task"
3. Select team member
4. Enter task details
5. Set deadline
6. Submit

##### Creating Projects
1. Navigate to "Projects"
2. Click "Create Project"
3. Fill project details:
   - Name, description
   - Start/end dates
   - Budget head
4. Create project groups
5. Assign members to groups

#### For HR

##### Managing Employee Information
1. Access "Employee Management"
2. Click "Add Employee" or select existing
3. Enter comprehensive details:
   - Personal information
   - Professional details
   - Upload documents
   - Salary structure
4. Save employee record

##### Reviewing Leave Requests
1. Dashboard shows pending HR approvals
2. Review Team Lead approved requests
3. Check leave balance
4. Approve/reject
5. Add HR signature

##### Managing Attendance
1. Go to "Attendance"
2. Select date
3. View attendance records
4. Mark attendance status
5. Generate reports

#### For Accounts

##### Processing Conveyance Claims
1. View "Conveyance Requests"
2. Review claims marked as seen by HR
3. Verify claim details
4. Check budget allocation
5. Approve payment
6. Mark as processed

##### Verifying Asset Request Budgets
1. Access "Asset Requests" (Accounts section)
2. Review procurement-approved requests
3. Enter budget details:
   - Budget allocation
   - Budget utilized
   - Available balance
4. Verify funds availability
5. Approve or request modification

#### For Procurement

##### Processing Asset Requests
1. View "Pending Procurement"
2. Open Team Lead justified request
3. Enter vendor quotations (up to 3)
4. Fill vendor details for each:
   - Vendor name
   - Item specifications
   - Unit price, quantity, total
5. Submit for Team Lead selection

#### For Directors/MD

##### Final Approvals
1. Dashboard shows all pending final approvals
2. Review complete request history
3. View all previous approvals
4. Make final decision
5. Add signature and comments

##### Performing Evaluations
1. Access "Evaluations"
2. Select employee evaluation
3. Review self and Team Lead evaluations
4. Fill Director evaluation form
5. Submit assessment

##### Viewing Analytics
1. Access "Analytics Dashboard"
2. View:
   - Company-wide metrics
   - Department statistics
   - Approval pending counts
   - Project progress
3. Generate reports

### Tips for Effective Use

#### Best Practices
- **Regular Updates**: Keep employee information current
- **Timely Approvals**: Process requests within SLA
- **Document Everything**: Add comments to approvals
- **Check Dashboard Daily**: Stay updated on pending items
- **Use Announcements**: Communicate important updates
- **Backup Data**: Regular database backups
- **Review Analytics**: Monitor trends and metrics

#### Common Troubleshooting

##### Cannot Login
- Verify email and password
- Check if account is deleted
- Contact admin for role assignment

##### Request Not Showing
- Check status filters
- Verify user role permissions
- Refresh dashboard

##### File Upload Failed
- Check file size (max 16MB)
- Verify file type is allowed
- Ensure stable internet connection

##### Permission Denied
- Verify user role
- Check with admin for permissions
- Clear browser cache and retry

---

## 🤝 Contributing

We welcome contributions to improve this ERP system! Here's how you can contribute:

### How to Contribute

#### 1. Fork the Repository
```bash
# Fork on GitHub, then clone
git clone https://github.com/YOUR-USERNAME/ERP-Web-Project.git
cd ERP-Web-Project
```

#### 2. Create a Feature Branch
```bash
git checkout -b feature/AmazingFeature
```

#### 3. Make Changes
- Follow existing code style
- Add comments for complex logic
- Update documentation
- Test thoroughly

#### 4. Commit Changes
```bash
git add .
git commit -m "Add: Brief description of changes"
```

**Commit Message Convention:**
- `Add:` New feature
- `Fix:` Bug fix
- `Update:` Existing feature improvement
- `Docs:` Documentation changes
- `Refactor:` Code refactoring
- `Test:` Adding tests

#### 5. Push to Branch
```bash
git push origin feature/AmazingFeature
```

#### 6. Open Pull Request
- Go to GitHub repository
- Click "New Pull Request"
- Describe changes thoroughly
- Reference any related issues

### Development Guidelines

#### Code Style
```python
# Use descriptive variable names
user_leave_balance = calculate_leave_balance(user_id)

# Add docstrings
def calculate_leave_balance(user_id):
    """
    Calculate remaining leave balance for user.
    
    Args:
        user_id (int): User ID
        
    Returns:
        int: Remaining leave balance
    """
    pass

# Follow PEP 8
# Use 4 spaces for indentation
# Max line length: 100 characters
```

#### Testing
```python
# Add tests for new features
import unittest

class TestLeaveRequest(unittest.TestCase):
    def test_submit_leave_request(self):
        # Test code
        pass
```

#### Documentation
- Update README for new features
- Add inline comments
- Update API documentation
- Create usage examples

### Areas for Contribution

#### High Priority
- [ ] Add unit tests
- [ ] Add integration tests
- [ ] Improve error handling
- [ ] Add API rate limiting
- [ ] Implement CSRF protection
- [ ] Add email notifications
- [ ] Mobile responsive improvements

#### Medium Priority
- [ ] Add export to Excel
- [ ] Bulk operations
- [ ] Advanced search filters
- [ ] Calendar integration
- [ ] SMS notifications
- [ ] Multi-language support
- [ ] Dark mode

#### Low Priority
- [ ] UI/UX improvements
- [ ] Additional chart types
- [ ] Custom report builder
- [ ] Integration with third-party services
- [ ] Mobile app
- [ ] Chat functionality

### Bug Reports

When reporting bugs, include:
- Description of the issue
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots (if applicable)
- Environment details (OS, browser, Python version)

**Use the GitHub issue template:**
```markdown
**Bug Description**
Clear description of the bug

**To Reproduce**
1. Go to '...'
2. Click on '...'
3. See error

**Expected Behavior**
What should happen

**Screenshots**
If applicable

**Environment:**
- OS: [e.g., Windows 10]
- Browser: [e.g., Chrome 90]
- Python Version: [e.g., 3.9]
```

### Feature Requests

- Check existing issues first
- Provide detailed description
- Explain use case
- Suggest implementation approach

---

## 📄 License

This project is **proprietary and confidential**. All rights reserved.

### Usage Terms
- This software is for internal organizational use only
- No redistribution without permission
- No commercial use without license
- Source code is confidential
- Contact the development team for licensing inquiries

---

## 👥 Authors & Acknowledgments

### Primary Developer
**Bhargavi Korimi**
- GitHub: [@bhargavikorimi](https://github.com/bhargavikorimi)
- Email: [Contact through GitHub]

### Contributors
- Team members who contributed to testing and feedback
- Organizations using this system for valuable insights

### Acknowledgments

#### Technologies
- **Flask** - Excellent Python web framework
- **Firebase** - Reliable backend services
- **SQLAlchemy** - Powerful ORM
- **Google APIs** - Integration capabilities
- **ReportLab & WeasyPrint** - PDF generation

#### Inspiration
- Modern ERP systems
- Organizational workflow requirements
- Employee feedback and suggestions

#### Special Thanks
- Testing team for thorough QA
- Early adopters for feedback
- Open-source community for excellent tools

---

## 📧 Support & Contact

### Getting Help

#### Documentation
- Read this README thoroughly
- Check inline code comments
- Review API documentation

#### Issues
- Search existing GitHub issues
- Create new issue with details
- Follow issue template

#### Contact
- GitHub Issues: [Project Issues](https://github.com/bhargavikorimi/ERP-Web-Project/issues)
- Email: [Contact through GitHub profile]

### Support Tiers

#### Community Support (Free)
- GitHub issues
- Documentation
- Community discussions

#### Professional Support (Paid)
- Dedicated support channel
- Priority bug fixes
- Custom feature development
- Deployment assistance
- Training sessions

Contact for professional support inquiries.

---

## 📊 Project Statistics

- **Total Lines of Code**: 6000+ lines in app.py
- **Database Tables**: 20+ tables
- **API Endpoints**: 134+ routes
- **User Roles**: 7 distinct roles
- **Features**: 20+ major feature categories
- **File Types Supported**: 8 document formats
- **Max File Upload**: 16MB
- **Evaluation Criteria**: 13 self-assessment + 7 HR + director assessments

---

## 🗺️ Roadmap

### Version 2.0 (Planned)
- [ ] Email notification system
- [ ] SMS alerts
- [ ] Advanced analytics dashboard
- [ ] Export to Excel functionality
- [ ] Bulk operations
- [ ] Calendar integration
- [ ] Mobile app (iOS/Android)

### Version 2.1 (Future)
- [ ] AI-powered insights
- [ ] Chatbot support
- [ ] Video conferencing integration
- [ ] Advanced reporting
- [ ] Custom workflow builder
- [ ] Multi-language support
- [ ] Dark mode theme

### Version 3.0 (Long-term)
- [ ] Microservices architecture
- [ ] GraphQL API
- [ ] Real-time collaboration
- [ ] Blockchain for audit trails
- [ ] Machine learning predictions
- [ ] Advanced security features
- [ ] Cloud-native deployment

---

## 📝 Changelog

### Current Version (1.0.0)
- Initial release
- Complete ERP functionality
- Multi-role authentication
- Request management system
- Project and task management
- Employee information system
- Attendance tracking
- Performance evaluation
- Asset request workflow
- Vendor management
- PDF report generation
- Role-based permissions
- Multi-dashboard support

---

## ⚠️ Important Notes

### Production Deployment
1. **Never commit sensitive files:**
   - `firebase-service-account.json`
   - `users.db`
   - `.env` files
   - API keys

2. **Security first:**
   - Change default secret key
   - Enable HTTPS
   - Implement rate limiting
   - Add CSRF protection
   - Regular security audits

3. **Data backup:**
   - Daily database backups
   - File upload backups
   - Version control
   - Disaster recovery plan

4. **Performance:**
   - Monitor application performance
   - Optimize database queries
   - Use caching where appropriate
   - Scale as needed

5. **Compliance:**
   - GDPR compliance (if applicable)
   - Data retention policies
   - Access audit logs
   - Privacy policy

---

## 🌟 Why Choose This ERP?

### Advantages
- ✅ **Comprehensive** - All-in-one solution
- ✅ **Customizable** - Easy to modify and extend
- ✅ **Secure** - Built with security best practices
- ✅ **Scalable** - Grows with your organization
- ✅ **User-friendly** - Intuitive interface
- ✅ **Well-documented** - Extensive documentation
- ✅ **Cost-effective** - Open for internal use
- ✅ **Modern stack** - Latest technologies

### Use Cases
- Small to medium enterprises
- Project-based organizations
- Multi-department companies
- Growing startups
- Educational institutions
- Non-profit organizations

---

**Built with ❤️ using Flask and Python**

---

*Last Updated: October 2025*

*For the latest updates, visit the [GitHub repository](https://github.com/bhargavikorimi/ERP-Web-Project)*
