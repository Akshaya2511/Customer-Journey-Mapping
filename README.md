# Customer Journey Mapping using Salesforce

## 📖 Project Overview

Customer interactions in many organizations are scattered across multiple systems and Salesforce objects such as Cases and Activities. This fragmentation makes it difficult to understand the complete customer journey and limits actionable insights.

This project implements a **Customer Journey Mapping solution using Salesforce** by creating a centralized mechanism to track, automate, and analyze customer interactions. Each significant interaction is captured as a **Touchpoint**, providing a unified and chronological view of customer engagement.

## 🎯 Problem Statement

Organizations face challenges in:

* Tracking customer interactions across different stages
* Maintaining a single source of truth for customer engagement
* Analyzing customer journey patterns
* Automating interaction logging without manual effort

## ✅ Solution Summary

The solution uses Salesforce’s declarative and programmatic capabilities to:

* Capture customer interactions automatically
* Store interactions in a custom **Touchpoint** object
* Link interactions directly to **Contacts**
* Provide analytical insights through reports

## 🏗️ Project Architecture

```
Case (Support Interaction)
   ↓
Contact (Customer)
   ↓
Touchpoint (Journey Event)
```

Whenever a **Case is closed**, a **Touchpoint** is automatically created and linked to the related Contact.

## 🔑 Key Features

* Custom **Touchpoint** object for journey tracking
* Lookup relationship between Touchpoint and Contact
* Record-Triggered Flow for Case automation
* Apex Trigger for Opportunity stage tracking
* Salesforce Reports for analytics
* Lightning UI customization for easy access

## 🧩 Salesforce Components Used

### 🔹 Custom Object

* **Touchpoint**

  * Stage
  * Interaction Date
  * Source
  * Related Contact
  * Description

### 🔹 Automation

* **Record-Triggered Flow**

  * Triggered when a Case is closed
* **Apex Trigger**

  * Triggered when Opportunity stage changes to *Closed Won*

### 🔹 Reporting

* Touchpoints by Stage (Summary Report)
* Touchpoints by Contact (Recent)

### 🔹 UI Customization

* Touchpoints related list on Contact page
* Lightning App Builder customization

## 📊 Business Value

* Centralized customer journey visibility
* Reduced manual data entry
* Improved customer experience
* Better decision-making through analytics
* Scalable CRM architecture

## 🧪 How It Works (End-to-End Flow)

1. Customer raises a support Case
2. Case is resolved and marked **Closed**
3. Salesforce Flow triggers automatically
4. A Touchpoint record is created
5. Touchpoint is linked to the Contact
6. Customer journey data becomes reportable

