# 🛠️ Contoso Issue Reporting — Maintenance Tracker Canvas App (Power Apps + Copilot)

> **A mobile-friendly canvas application built with Microsoft Copilot in Power Apps, enabling Contoso College employees to report campus maintenance issues and manage asset records.**

---

## 📌 Project Overview

This project demonstrates how to use **Microsoft Copilot in Power Apps** to rapidly design a data model and build a fully functional canvas application from scratch using natural language prompts. The app is designed to run on mobile devices, allowing employees across Contoso College's campus to submit maintenance requests and manage asset records — all from a single, intuitive interface.

---

## 🎯 Learning Objectives

- Use **Copilot** to generate a data model and scaffold an app automatically
- Modify and personalize a **canvas application** layout and screens
- Configure **table relationships** between Dataverse tables
- Add and customize **new screens** using Copilot
- **Test, save, and publish** a Power Apps canvas app

---

## 🗂️ Data Model

### Primary Table — `Maintenance Issue`

| Column               | Type   | Description                                  |
|----------------------|--------|----------------------------------------------|
| Issue Type           | Choice | Category of the maintenance issue            |
| Location             | Text   | Where on campus the issue is located         |
| Contact Number       | Text   | Reporter's contact number                    |
| Priority Level       | Choice | Urgency level of the issue                   |
| Access Instructions  | Text   | Notes for technician access                  |
| Resolution Notes     | Text   | Notes added upon resolving the issue         |

### Supporting Table — `User` *(Existing Dataverse Table)*

| Relationship                   | Display Name        | Schema Name  |
|--------------------------------|---------------------|--------------|
| User → Maintenance Issue       | Requesting Employee | *(default)*  |
| User → Maintenance Issue       | Assigned To         | AssignedUser |

### Additional Table — `Assets`

| Column         | Type | Description                        |
|----------------|------|------------------------------------|
| Asset Name     | Text | Name of the asset                  |
| Asset ID       | Text | Unique identifier for the asset    |
| Asset Type     | Text | Type/category of the asset         |
| Asset Location | Text | Where the asset is located         |
| Date Installed | Date | Installation date of the asset     |
| Department     | Text | Department responsible for asset   |

---

## 📱 App Screens

### 1. Welcome Screen
- Displays navigation tiles for **Submit Maintenance Issue** and **Assets**
- Custom stock images for each navigation item
- Header branded as **"Contoso Issue Reporting"** with black fill
- Logo and profile picture hidden for a clean mobile experience

![My Image](https://github.com/R887645/Contoso-Issue-Reporting-Maintenance-Tracker-Canvas-App-Power-Apps-Copilot-/blob/main/Screenshot%202026-03-28%20083759.png?raw=true)

### 2. Maintenance Issues Screen
- Auto-generated from the Maintenance Issue table
- Allows employees to submit and view issue records

![My Image](https://github.com/R887645/Contoso-Issue-Reporting-Maintenance-Tracker-Canvas-App-Power-Apps-Copilot-/blob/main/Screenshot%202026-03-28%20073423.png?raw=true)

### 3. Assets Screen
- Displays an asset gallery with a custom `Text Label` showing `Asset Type`
- Single-column form layout for clean mobile readability
- Supports search, edit, and save of asset records

![My Image](https://github.com/R887645/Contoso-Issue-Reporting-Maintenance-Tracker-Canvas-App-Power-Apps-Copilot-/blob/main/Screenshot%202026-03-28%20113956.png?raw=true)

---

## 🔗 Navigation Flow

```
[Welcome Screen]
     ├── Submit Maintenance Issue  →  [Maintenance Issues Screen]
     └── Assets                   →  [Assets Screen]
```
[Walkthrough Video of the Project](https://drive.google.com/file/d/1fZti3fEJPwticEBP3DZMyqaEAB2VMq5k/view?usp=sharing)
---

## 🛠️ Technologies Used

| Tool / Service          | Purpose                                    |
|-------------------------|--------------------------------------------|
| Microsoft Power Apps    | Canvas app hosting and development         |
| Microsoft Copilot (PA)  | AI-assisted data model + screen generation |
| Microsoft Dataverse     | Backend data storage                       |
| Power Apps Studio       | App design, properties, and formula editor |

---

## 🧪 Testing

The app was tested in **Preview mode** within Power Apps Studio:

| Test Step                               | Result  |
|-----------------------------------------|---------|
| Navigate to Assets screen from Welcome  | ✅ Pass |
| Search for asset by keyword ("Office")  | ✅ Pass |
| Open and edit an asset record           | ✅ Pass |
| Save changes to asset                   | ✅ Pass |
| Return to Welcome screen via Home       | ✅ Pass |

---

## ✅ Project Status

| Task                                    | Status      |
|-----------------------------------------|-------------|
| Data model created with Copilot         | ✅ Complete |
| Table relationships configured          | ✅ Complete |
| App scaffolded from Copilot             | ✅ Complete |
| Welcome screen personalized             | ✅ Complete |
| Assets screen added and configured      | ✅ Complete |
| Navigation updated on Welcome screen    | ✅ Complete |
| App tested in preview mode              | ✅ Complete |
| App saved and published                 | ✅ Complete |

---

## 🚀 How to Run

1. Sign in to the [Power Apps Maker Portal](https://make.powerapps.com)
2. Navigate to **My Apps** and open **Contoso Issue Reporting**
3. Select **Play** to run in browser, or open via the **Power Apps mobile app**
4. Use the Welcome Screen to navigate to Maintenance Issues or Assets

---

## 👤 Author

**Rofiah Kehinde**
Power Platform learner | Canvas App development exercise — Contoso College scenario

---

## 📄 License

This project was created for educational purposes as part of a Microsoft Power Platform learning module.
