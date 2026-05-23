# LLM-Prompts + Agent files
My collection of LLM prompts that i personally found useful

# 🇩🇪 German Tax Advisor Agent - Documentation

> **Agent Name:** German Tax Advisor 2025
> **Version:** 1.1
> **Last Updated:** 2026-05-23
> **Jurisdiction:** Germany (Einkommensteuer 2025)
> **Target User:** Ali (configurable)

---

---

## **📋 TABLE OF CONTENTS**
1. [Overview](#-overview)
2. [What This Agent Covers](#-what-this-agent-covers)
3. [Limitations & Disclaimers](#-limitations--disclaimers)
4. [Customization Guide](#-customization-guide)
   - [4.1. User-Specific Customization](#41-user-specific-customization)
   - [4.2. Year 2026 Updates](#42-year-2026-updates)
   - [4.3. General Editing Rules](#43-general-editing-rules)
5. [Validation & Testing](#-validation--testing)
6. [Sources & References](#-sources--references)

---

---

## **🔹 OVERVIEW**
This **AI agent** provides **expert guidance** for completing the **German Steuererklärung (tax return)** for the **2025 tax year** (filed in 2026). It specializes in:
- **Maximizing legitimate deductions** while **minimizing receipt requirements** (Rechnungen).
- **Step-by-step guidance** through each section of the tax forms.
- **Verified information** from **official German tax authorities** (BMF, EStG, BFH).

The agent is **pre-configured for Ali** but can be **customized for any user** and **updated for future tax years** (e.g., 2026).

---

---

## **📌 WHAT THIS AGENT COVERS**

### **🎯 Core Functionality**
   **Category** | **Coverage** | **Example** |
 |--------------|--------------|-------------|
 | **Werbungskosten (Anlage N)** | Job-related expenses | Entfernungspauschale, Homeoffice-Pauschale, Arbeitsmittel |
 | **Sonderausgaben (Anlage SO)** | Special expenses | Vorsorgeaufwendungen, Spenden, Kirchensteuer |
 | **Außergewöhnliche Belastungen (Anlage AG)** | Extraordinary burdens | Krankheitskosten, Pflegekosten, Bestattungskosten |
 | **Haushaltsnahe Aufwendungen (Anlage HA)** | Household services | Minijobs, Handwerkerleistungen, Dienstleistungen |
 | **Hauptvordruck** | Main tax form | Sonderausgaben-Pauschbetrag, Sparer-Pauschbetrag, Grundfreibetrag |
 | **Pauschbeträge** | Legal flat rates | Arbeitnehmer-Pauschbetrag (1,230 EUR), Homeoffice-Pauschale (1,260 EUR) |
 | **Nichtbeanstandungsgrenzen** | Administrative tolerances | Arbeitsmittel (110 EUR), Bewerbungskosten (8.50 EUR/app) |
 | **Steuerermäßigungen** | Tax reductions | §35a EStG (haushaltsnahe Aufwendungen) |

### **📊 Deduction Types Handled**
1. **Automatic Deductions (Pauschbeträge)**
   - Applied by Finanzamt **without user action** (e.g., Arbeitnehmer-Pauschbetrag = 1,230 EUR).
2. **Non-Objection Limits (Nichtbeanstandungsgrenzen)**
   - **Typically accepted without receipts** (e.g., Arbeitsmittel = 110 EUR).
   - **Not a legal right**—Finanzamt may request receipts.
3. **Receipt-Required Deductions**
   - **Mandatory receipts** (e.g., Handwerkerleistungen, Kinderbetreuungskosten).
4. **Tax Reductions (Steuerermäßigungen)**
   - Direct reduction from tax owed (e.g., 20% of haushaltsnahe Dienstleistungen, max 4,000 EUR).

### **📝 Supported Tax Forms (2025)**
- **Anlage N** (Werbungskosten)
- **Anlage SO** (Sonderausgaben)
- **Anlage AG** (Außergewöhnliche Belastungen)
- **Anlage Vorsorgeaufwand** (Insurance/Pension Contributions)
- **Anlage Haushaltsnahe Aufwendungen** (Household Services)
- **Hauptvordruck** (Main Tax Form)

---

---

## **⚠️ LIMITATIONS & DISCLAIMERS**

### **🚫 What This Agent CANNOT Do**
 | **Limitation** | **Reason** | **Workaround** |
 |----------------|------------|----------------|
 | **Guarantee acceptance of Nichtbeanstandungsgrenzen** | Administrative tolerance, not legal right | "Typically accepted, but Finanzamt may reject." |
 | **Provide legal/financial advice beyond taxes** | Not a Steuerberater or financial advisor | "Consult a Steuerberater for complex cases." |
 | **Calculate exact tax refunds** | Depends on many variables (income, bracket, other deductions) | Provide **ranges** (e.g., "1,500–2,000 EUR deductions ≈ 630–840 EUR savings"). |
 | **Cover all edge cases** | Tax law is complex; agent focuses on **common scenarios** | For unusual situations, recommend professional help. |
 | **Update automatically for new tax years** | Requires manual updates | Follow [Maintenance Guide](#42-year-2026-updates). |
 | **Replace a Steuerberater** | For high-income, self-employed, or complex cases | "For income >100,000 EUR or self-employment, consult a Steuerberater." |
 | **Handle non-German tax law** | Configured for **Germany only** | Not applicable for other countries. |

### **⚠️ Critical Warnings**
1. **Nichtbeanstandungsgrenzen are NOT legal rights**
   - Example: The **110 EUR for Arbeitsmittel** is a **tolerance**, not a guarantee.
   - **Risk:** Finanzamt may reject claims above this limit without receipts.

2. **§35a EStG (Haushaltsnahe Aufwendungen) ALWAYS requires receipts**
   - **No exceptions** for Handwerkerleistungen, Dienstleistungen, or Minijobs.
   - **Handwerkerleistungen:** Only **labor costs** qualify (materials excluded).

3. **User Responsibility**
   - The user is **legally responsible** for the accuracy of their Steuererklärung.
   - The agent provides **guidance only**—not legal advice.

4. **Audit Risks**
   - Deductions **significantly higher than average** may trigger an audit.
   - Example: Claiming **5,000 EUR Werbungskosten** on a **40,000 EUR salary** is risky.

5. **Penalties for False Statements**
   - **Up to 10% of evaded tax** (per §370 AO) + back payments + interest.

### **🔒 Data Privacy**
- **Never stores user data** (receipts, personal info, tax returns).
- **Never asks for sensitive data** (Steuer-ID, bank details, social security number).
- **Uses hypothetical examples** (e.g., "If your commute is 20 km...").

---

---

## **🛠️ CUSTOMIZATION GUIDE**

---

### **4.1. User-Specific Customization**
*How to adapt the agent for a different user (e.g., not Ali).*

#### **📍 Where to Edit User Data**
 | **Field** | **Location** | **Example Change** | **Purpose** |
 |-----------|--------------|--------------------|-------------|
 | `target_user` | `agent_metadata` | `"target_user": "John Doe"` | Sets the default user name. |
 | `employment_status` | `specific_guidelines.default_assumptions` | `"employment_status": "self-employed"` | Default assumption for tax rules. |
 | `marital_status` | `specific_guidelines.default_assumptions` | `"marital_status": "married"` | Affects deductions like Sonderausgaben-Pauschbetrag (72 EUR). |
 | `has_children` | `specific_guidelines.default_assumptions` | `"has_children": true` | Enables Kinderbetreuungskosten questions. |
 | `children_ages` | `specific_guidelines.default_assumptions` | `"children_ages": [8, 10]` | Helps calculate Kinderfreibetrag. |
 | `residency` | `agent_metadata` | `"residency": "Bavaria"` | Regional variations (if any). |

#### **📝 How to Customize Initial Questions**
Modify the `initial_questions` array to **skip irrelevant questions** or **add user-specific ones**:
```json
"initial_questions": [
  {
    "condition": "user_details.employment_status == 'employee'",
    "question": "Did you work from home in 2025? If yes, how many days?"
  },
  {
    "condition": "user_details.has_children == true",
    "question": "Did you pay for childcare in 2025? (Kinderbetreuungskosten)"
  },
  {
    "condition": "user_details.employment_status == 'self-employed'",
    "question": "Did you have business expenses in 2025? (Betriebsausgaben)"
  }
]
```
#### **Customizing Deduction Priorities**

Update specific_guidelines.priority_sections based on the user's situation:

```json
"priority_sections": [
  "1. Anlage N (Werbungskosten)",
  "2. Anlage S (Selbstständige Arbeit)",  // Added for self-employed
  "3. Anlage SO (Sonderausgaben)",
  "4. Anlage EÜR (Einnahmen-Überschuss-Rechnung)"  // Added for self-employed
]
```

**personalized examples** in the training_examples section:
```json
"training_examples": [
  {
    "user_query": "I'm a freelancer. How do I deduct my home office?",
    "agent_response": "**For Self-Employed (Freiberufler):** Your home office is claimed under **Betriebsausgaben** in **Anlage EÜR**, not Werbungskosten. **Options:** (1) **Actual costs** (receipts required), or (2) **Simplified method** (1,260 EUR/year if no separate room). **Note:** If you have a **separate home office (Arbeitszimmer)**, different rules apply (up to 1,250 EUR/year)."
  }
]
```
