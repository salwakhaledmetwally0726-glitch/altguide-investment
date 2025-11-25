
# [ALTGIUDE]

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

- **Concept:** ["AltGuide is a beginner-friendly investment guidance platform designed to help university students build smart savings habits using micro-investment features, educational insights, and automated financial planning."
-Most young users don’t know:

how to invest,

how to choose the right risk level,

how much money to start with,

or how to understand financial concepts.

This leads to fear, bad financial decisions, or zero savings.

Solution

AltGuide Investment provides:

Micro-investment (start with very small amounts)

AI-powered risk assessment

Beginner-friendly investment guides

Simulated portfolios to practice without losing money

Smart recommendations based on user profile

Core Value ]
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

### 3.2 Selected MVP Use Cases (Course Scope)

_From the list above, identify the **5 or 6 specific use cases** you will implement for this course. Note: User Authentication is mandatory._

1.  **User Authentication** (Registration/Login)
2.  User Authentication (Registration/Login)

Use Case 2 – User Investment Dashboard

Use Case 3 – Create & Manage Investment Plans

Use Case 4 – Transaction History & Tracking

Use Case 5 – Portfolio Performance Analytics

Use Case 6 – Financial Insights & Recommendation Engine 
---

## 4. Feature Assignments (Accountability)

_Assign one distinct use case from Section 3.2 to each team member. This member is responsible for the full-stack implementation of this feature._

| Team Member | Assigned Use Case       | Brief Description of Responsibility              |
| :---------- | :---------------------- | :----------------------------------------------- |
| [Salwa] | **User Authentication** | Register, Login, JWT handling, Password Hashing. |
| [Lojaina] | [Risk Assessment Quiz]            | [Collect user data & calculate risk score]      |
| [Mai] | [Investment Recommendations]            | [Generate suitable investment options based on risk score]           |
| [shorouk] | [Portfolio Overview Page]            | [Display user investments, categories & performance]                     |
| [Mohamed] | [Market Insights Feed]            | [Fetch / display relevant market news to help decision-making]                                    |
| [Omar] | [User Profile Management]            | [Update profile, investment goals, preferences]                                    |

---

## 5. Data Model (Initial Schemas)

_Define the initial Mongoose Schemas for your application’s main data models (User, Transaction, Account, etc.). You may use code blocks or pseudo-code._

### User Schema

```javascript
const UserSchema = new mongoose.Schema({
  username: { type: String, required: true, unique: true },
  email: { type: String, required: true, unique: true },
  password: { type: String, required: true },
  riskLevel: { type: String, enum: ["Low", "Medium", "High"], default: "Low" },
  createdAt: { type: Date, default: Date.now }
});

});
```

### [portofolio] Schema
const PortfolioSchema = new mongoose.Schema({
  userId: { type: mongoose.Schema.Types.ObjectId, ref: "User" },
  balance: { type: Number, default: 10000 }, // simulated money
  investments: [
    {
      assetName: String,
      amount: Number,
      date: Date
    }
  ]
});

### [transaction] Schema

```javascript
const TransactionSchema = new mongoose.Schema({
  userId: { type: mongoose.Schema.Types.ObjectId, ref: "User" },
  type: { type: String, enum: ["Buy", "Sell"], required: true },
  assetName: String,
  amount: Number,
  date: { type: Date, default: Date.now }
});

