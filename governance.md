# 🏢 Management & Governance – Deep Dive

A detailed and exam-focused breakdown of AWS Management & Governance services.

---

## 🔹 AWS Organizations

AWS Organizations helps manage multiple AWS accounts centrally.

It enables governance, billing control, and policy enforcement across accounts.

---

### 🏗 Core Components

- **Organization**
- **Root**
- **Organizational Units (OUs)**
- **Accounts**
- **Service Control Policies (SCPs)**

---

### 🔐 Service Control Policies (SCPs)

- Define maximum permissions
- Do NOT grant permissions
- Apply to accounts or OUs
- Restrict what IAM users can do

---

### 💰 Consolidated Billing

- Single bill for multiple accounts
- Volume discounts
- Centralized payment method

---

### 📌 Exam Focus

- SCPs restrict permissions
- Best practice: Separate accounts for prod, dev, security
- Use OUs to group accounts
- Centralized governance model

---

### 🌍 Real-World Example

Enterprise managing 50 AWS accounts under one organization with restricted production access.

---

---

## 🔹 AWS Control Tower

Control Tower automates multi-account setup.

Built on top of AWS Organizations.

---

### ⚙️ Key Features

- Landing zone setup
- Pre-configured guardrails
- Account factory
- Centralized logging
- Multi-account governance

---

### 🛡 Guardrails

- Preventive (SCP-based)
- Detective (Config-based)

---

### 📌 Exam Focus

- Simplifies enterprise AWS environment setup
- Automated governance
- Uses Organizations under the hood
- Landing Zone concept

---

### 🌍 Real-World Example

Large enterprise setting up secure AWS environment for multiple business units automatically.

---

---

## 🔹 AWS Budgets

AWS Budgets helps monitor and control AWS spending.

---

### ⚙️ Key Features

- Set cost budgets
- Set usage budgets
- Forecasted alerts
- SNS notifications
- Automated actions

---

### 📌 Exam Focus

- Alerts before exceeding budget
- Can trigger actions
- Different from Cost Explorer (analysis vs alerts)

---

### 🌍 Real-World Example

Startup setting monthly $5,000 budget and receiving alerts at 80% usage.

---

---

## 🔹 AWS Cost Explorer

Cost Explorer provides cost visualization and analysis.

---

### 📊 Key Features

- Historical cost analysis
- Forecast future spending
- Filter by service, region, tag
- Reserved Instance recommendations

---

### 📌 Exam Focus

- Used for cost analysis
- Visual reports
- Not real-time alerts (Budgets does alerts)

---

### 🌍 Real-World Example

Finance team analyzing monthly spending trends across departments.

---

---

## 🔹 AWS License Manager

License Manager helps manage software licenses in AWS.

---

### ⚙️ Key Features

- Track license usage
- Enforce license limits
- Supports BYOL (Bring Your Own License)
- Integrates with EC2

---

### 📌 Exam Focus

- Helps maintain compliance
- Track license usage across accounts
- Often used in large enterprises

---

### 🌍 Real-World Example

Company tracking Microsoft SQL Server licenses across multiple EC2 instances.

---

# ✅ Management & Governance Section Complete
