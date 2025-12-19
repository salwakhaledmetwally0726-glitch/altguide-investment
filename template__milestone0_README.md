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

---

## 2. Project Description

_Provide a detailed description of your project concept here. What is the app? What problem does it solve?_

- **Concept:** ["AltGuide is a beginner-friendly investment guidance platform designed to help university students build smart savings habits using micro-investment features, educational insights,financial planning."
-Most young users don’t know:

how to invest,

how to choose the right risk level,

how much money to start with,

or how to understand financial concepts.

This leads to fear, bad financial decisions, or zero savings.

Solution

AltGuide Investment provides:

help you start with Micro-investment (start with very small amounts)

Beginner-friendly investment guides

Smart recommendations based on user profile

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

notifications and reminders for the investments 

### 3.2 Selected MVP Use Cases (Course Scope)

_From the list above, identify the **5 or 6 specific use cases** you will implement for this course. Note: User Authentication is mandatory._

1.  User Authentication (Registration/Login)

Use Case 2 – User Risk profile mangemnet 
users can define thier risk level low medium or high to refect their investment prefrences 

Use Case 3 – Investment Goals Management
		Users can create investment goals with target amounts and deadlines.
	  Users can view, update, and delete their goals.

Use Case 4 – Holdings Management
		Users can record the investments they currently own (e.g., stocks, gold, ETFs).
		Each holding includes quantity, buy price, and current price.
		Users can add, update, view, and delete holdings.
  
Use Case 5 – Goal Progress Tracking:
Allows users to track how close they are to achieving each investment goal by calculating and displaying a progress percentage based on the current and target amounts.

## 4. Feature Assignments (Accountability)

_Assign one distinct use case from Section 3.2 to each team member. This member is responsible for the full-stack implementation of this feature._

| Team Member | Assigned Use Case       | Brief Description of Responsibility              |
| :---------- | :---------------------- | :----------------------------------------------- |
| [mai] | **User Authentication** | Handles user registration and login functionality, including storing user credentials and validating login requests. |
  | [Lojaina] | [Risk Assessment ]            | [Manages the user’s risk preference (low, medium, high) and allows storing and viewing this information.]    |
| [salwa ] | [investment goals MANGEMENT ]            | [Responsible for creating, viewing, updating, and deleting investment goals defined by the user.]           |
| [shorouk] | [holding Mnagement]            | [Manages the user’s current investment holdings, allowing adding, viewing, updating, and deleting owned assets.]                     |
| [salwa mai] | [goal progress tracking ]            | [mplements the calculation and display of progress percentage for each investment goal based on current and target amounts.]                                    |
                             

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
```javascript
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
