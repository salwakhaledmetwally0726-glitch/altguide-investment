# Template README for BINF 503 Project

## Open on GitHub: [template\_\_README.md](https://github.com/nourgaser-giu/giu-bi-ebd-w2025/blob/main/template__milestone0_README.md)

## Download (ctrl+s to save): [template\_\_README.md](https://raw.githubusercontent.com/nourgaser-giu/giu-bi-ebd-w2025/main/template__milestone0_README.md)

<!-- Delete all of the above for your submission -->

# [Insert Project Name Here]

**Course:** Electronic Business Development (BINF 503)  
**Semester:** Winter 2025  
**Instructor:** Dr. Nourhan Hamdi  
**Teaching Assistants:** Mr. Nour Gaser, Mr. Omar Alaa

---

## 1. Team Members

_List all team members (5-6 students) below._

| Name             | Student ID | Tutorial Group | GitHub Username |
| :--------------- | :--------- | :------------- | :-------------- |
| [salwa khaled] | [13007498]       | [T6]           | [salwakhaledmetwally0726-glitch]     |
| [lojaina mohamed] | [13007458]       | [T6]           | [Lojaina108]     |
| [mai mohamed] | [13006213]       | [T6]           | [maixmohamed23-sys]     |
| [shorouk gamal] | [13007144]       | [T6]           | [shroukgamal2005-ui]    |
| [mohamed walid] | [13007046]       | [T6]           | [Wxllo]     |
| [omar ehab] | [ 13006897]       | [T3]           | [OmarFernandes8]     |

---

## 2. Project Description

_Provide a detailed description of your project concept here. What is the app? What problem does it solve?_

- **Concept:** ["AltGuide is a beginner-friendly investment guidance platform designed to help university students build smart savings habits using micro-investment features, educational insights, and automated financial planning."]
- **Link to Fin-Tech Course Document:** []

---

## 3. Feature Breakdown
These are ALL features your full application could include in the future beyond the course MVP:

User Authentication

Registration, Login, JWT, password hashing

Investment Recommendation Engine

Suggests investments based on user risk score

User Profile & Risk Assessment

Questionnaire to measure risk level

Goal-Based Investing

Set savings goals (education, travel, startup capital, emergency fund…)

Transaction Simulator
Investment Portfolio Dashboard

Charts showing projected growth, risk, asset distribution


Optional extra features
### 3.1 Full Scope
User Authentication (Mandatory)

User Risk Profile Assessment

Investment Recommendations Page

Goal Setting & Tracking

Educational Content Module

Dashboard Overview (Summary of user data)
_List ALL potential features/user stories envisioned for the complete product (beyond just this course)._

- Feature A
- Feature B
- Feature C
- ...

### 3.2 Selected MVP Use Cases (Course Scope)

_From the list above, identify the **5 or 6 specific use cases** you will implement for this course. Note: User Authentication is mandatory._

1.  **User Authentication** (Registration/Login)
2.  [Use Case 2 Title]
3.  [Use Case 3 Title]
4.  [Use Case 4 Title]
5.  [Use Case 5 Title]
6.  [Use Case 6 Title - if 6 members]

---

## 4. Feature Assignments (Accountability)

_Assign one distinct use case from Section 3.2 to each team member. This member is responsible for the full-stack implementation of this feature._

| Team Member | Assigned Use Case       | Brief Description of Responsibility              |
| :---------- | :---------------------- | :----------------------------------------------- |
| [Student 1] | **User Authentication** | Register, Login, JWT handling, Password Hashing. |
| [Student 2] | [Use Case 2]            | [e.g., Create and view Transaction history]      |
| [Student 3] | [Use Case 3]            | [e.g., Profile management and updates]           |
| [Student 4] | [Use Case 4]            | [e.g., Transfer funds logic]                     |
| [Student 5] | [Use Case 5]            | [Description]                                    |
| [Student 6] | [Use Case 6]            | [Description]                                    |

---

## 5. Data Model (Initial Schemas)

_Define the initial Mongoose Schemas for your application’s main data models (User, Transaction, Account, etc.). You may use code blocks or pseudo-code._

### User Schema

```javascript
const UserSchema = new mongoose.Schema({
  username: { type: String, required: true },
  email: { type: String, required: true, unique: true },
  password: { type: String, required: true },
  // Add other fields...
});
```

### [Model 2 Name] Schema

```javascript
// Define schema here
```

### [Model 3 Name] Schema

```javascript
// Define schema here
```
