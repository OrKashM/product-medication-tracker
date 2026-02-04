# Product Medication Tracker

> Product MVP — Patient-centered medication tracking system  
> Intelligent stock management and treatment adherence monitoring.

---

## 🧠 Context & Problem

Patients undergoing long-term or complex treatments often face:
- missed medication intakes
- poor visibility on remaining medication stock
- preventable stock shortages
- high mental load for accompanying caregivers

Most existing solutions are either too complex, not adapted to real daily usage,
or focused on medical professionals rather than patients and caregivers.

---

## 🎯 Product Objective

Design a **simple, reliable, and human-centered system** that helps:
- patients confirm their medication intake easily
- caregivers monitor adherence and stock levels
- anticipate stock shortages before they happen

This project focuses on **product clarity, MVP scope, and technical trade-offs**.

---

## 👥 Target Users

- **Patient**
  - Confirms medication intake
  - Views personal intake history

- **Accompanying caregiver**
  - Configures treatments
  - Manages medication stock
  - Monitors adherence and alerts

> No doctors or pharmacies are included in the MVP by design.

---

## 🧩 MVP Scope

### Medication Stock Management
- Medication creation (name, form, unit)
- Available quantity tracking
- Expiration date
- Low-stock threshold alerts
- Automatic stock decrement on confirmed intake

### Treatment Adherence Tracking
- Treatment schedules (time & frequency)
- Intake confirmation (TAKEN / MISSED)
- Intake history
- Alerts on repeated missed intakes

---

## 🚫 Out of MVP Scope (Intentional)

- Automatic medication ordering
- Medical recommendations
- Barcode / box scanning
- Advanced clinical analytics

The MVP **observes and alerts** — it does not prescribe.

---

## 🧠 Core Business Rules

- Stock is managed as a **single source of truth**
- Confirmed intake decreases stock automatically
- Missed intake does not affect stock
- Stock can never be negative
- Liquid medications are handled using dose-per-intake logic
- Alerts are persistent and traceable

Detailed rules are documented in `/docs/business-rules.md`.

---

## 🏗️ Architecture Overview

- **Backend**: Django REST API (source of truth)
- **Business logic**: service-based architecture
- **Clients**: future mobile & web applications
- **Database**: relational, product-driven data model

Architecture diagrams are available in `/diagrams`.

---

## 📐 Design & Diagrams

See `/diagrams` for:
- Use case diagram
- Data model diagram
- Application architecture
- Stock flow logic

---

## 🧪 Quality & Reliability

The MVP is covered by **business-oriented tests** validating:
- stock integrity
- intake adherence logic
- alert triggering
- role-based permissions

The goal is to ensure **product reliability without relying on UI**.

---

## 🛣️ Product Roadmap (Post-MVP)

Planned evolutions include:
- multi-patient support
- analytics dashboards
- advanced notifications
- healthcare professional read-only access
- Albertine Home Inventory Mode

See `/docs/roadmap.md` for details.

---

## 📌 Product Engineer Perspective

This repository demonstrates:
- MVP design and development
- translation of real human problems into technical solutions
- product decisions and technical trade-offs
- long-term vision, roadmap, and iteration

---

## 📄 License

This project is released under the MIT License.
