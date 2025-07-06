# Requirement Analysis in Software Development

Requirement Analysis is a critical phase in the software development lifecycle (SDLC) where stakeholders, business analysts, and developers collaborate to define, document, and validate the needs and expectations for a software system. Its primary goals are:

Clarity & Understanding – Ensures all stakeholders (clients, users, developers) have a shared vision of the software’s functionality, constraints, and objectives.

Scope Definition – Prevents misunderstandings by clearly outlining what the system will (and will not) do, reducing the risk of scope creep.

Feasibility Assessment – Evaluates technical, economic, and operational practicality before development begins.

Foundation for Design & Development – Serves as a blueprint for architects, developers, and testers to build and validate the system.

Risk Mitigation – Identifies potential conflicts, ambiguities, or gaps early, saving time and costs in later stages.

# What is Requirement Analysis? 

Requirement Analysis is the process of identifying, documenting, and validating the needs and constraints of stakeholders to define what a software system must do. It is a crucial phase in the Software Development Life Cycle (SDLC) that ensures the final

# Why is Requirement Analysis Important?,

  1. Ensures You Build the Right Product
Prevents costly misunderstandings by clarifying exactly what needs to be built

Aligns developer understanding with stakeholder expectations

Example: Without proper analysis, you might build a web app when stakeholders actually needed a mobile app

2. Saves Time and Money
Fixing errors in requirements costs 10-100x more if discovered late in development (IBM Systems Sciences Institute)

Reduces unnecessary rework by identifying problems early

Example: Catching a missing regulatory requirement early avoids legal penalties later

3. Improves Project Success Rates
71% of failed projects cite poor requirements as primary cause (PMI)

Clear requirements lead to more accurate timelines and budgets

Example: Well-defined scope prevents endless "just one more feature" requests

# Key Activities in Requirement Analysis.


1. Requirement Gathering
Collecting raw needs from stakeholders (users, clients, domain experts)

Methods: Interviews, surveys, workshops, observation

Output: Initial wishlist of features and constraints

2. Requirement Elicitation
Extracting hidden/implied needs through probing questions

Techniques: User stories, scenarios, prototyping

Focus: Understanding the "why" behind requests

3. Requirement Documentation
Structuring requirements into clear specifications

Formats: SRS documents, use cases, user stories

Key: Making requirements unambiguous and testable

4. Requirement Analysis & Modeling
Organizing requirements into logical structures

Tools: UML diagrams, flowcharts, data models

Purpose: Identifying relationships and conflicts

5. Requirement Validation
Verifying requirements are:

Complete ✔️

Consistent ✔️

Feasible ✔️

Testable ✔️

Methods: Reviews, prototyping, traceability matrices


# Types of Requirements.

1. Functional Requirements (What the system must DO)
Define the specific features and actions the system must perform.

Examples for a Booking Management System:

User Registration & Authentication

"Users must be able to register using email and password."

"Users should be able to reset passwords via email."

Booking Management

"Customers can search for available slots based on date/time."

"Admins can approve, reject, or modify bookings."

Payment Processing

"The system must integrate with PayPal and Stripe for payments."

"Users should receive a payment confirmation email."

Notifications

"Users should get SMS/email reminders 24 hours before booking."

"Admins should receive alerts for new booking requests."

2. Non-Functional Requirements (How the system must PERFORM)
Define quality attributes, constraints, and performance standards.

Examples for a Booking Management System:

Performance

"The system should handle 1,000 concurrent users without slowdown."

"Search results must load in under 2 seconds."

Security

"All user passwords must be encrypted (bcrypt/SHA-256)."

"Payment data must comply with PCI DSS standards."

Usability

"The booking form should be completable in under 3 steps."

"The UI must be mobile-responsive (support Android/iOS)."

Reliability

"The system must have 99.9% uptime (excluding maintenance)."

"Failed transactions should trigger automatic retries (max 3 attempts)."

Scalability

"The database should support 10,000+ bookings per month."

"The system should allow adding new payment gateways without downtime."

# Use Case Diagrams
A Use Case Diagram is a visual representation of a system’s functional requirements from a user’s perspective. It shows:

Actors (users, systems, or external entities)

Use Cases (actions the system performs)

Relationships between them

┌───────────────────────────────────┐  
│         Booking Management        │  
└────────────────┬──────────────────┘  
                 │  
    ┌────────────┴────────────┐  
    │       Book Appointment  │  
    └────────────┬────────────┘  
                 │  
    ┌────────────▼────────────┐  
    │       Cancel Booking    │◄──┐  
    └────────────┬────────────┘   │  
                 │                │  
    ┌────────────▼────────────┐   │  
    │     Process Payment     │   │  
    └────────────┬────────────┘   │  
                 │                │  
    ┌────────────▼────────────┐   │  
    │    Generate Invoice     │   │  
    └────────────────────────┘   │  
                                 │  
┌─────────┐             ┌────────▼───────┐  
│ Customer│             │      Admin     │  
└─────────┘             └────────────────┘  


[https://drive.google.com/file/d/1_DeZbisUi_7Sjq7cDBM0u3DjRVpzJ5M0/view?usp=sharing](https://drive.google.com/file/d/1_DeZbisUi_7Sjq7cDBM0u3DjRVpzJ5M0/view?usp=sharing)


# Acceptance Criteria.
Acceptance Criteria (AC) are clear, testable conditions that a feature must meet to be considered complete. They act as a contract between stakeholders and developers, ensuring:

Clarity & Precision – Eliminates ambiguity in requirements.

Alignment – Ensures developers and stakeholders agree on "done."

Testability – Provides a basis for QA validation.

Reduces Rework – Prevents misunderstandings that lead to costly fixes.

Agile Compliance – Critical for User Stories in Scrum/Kanban.

Example: Acceptance Criteria for a "Checkout" Feature (Booking System)
Feature: "As a customer, I want to complete my booking by paying online so I can confirm my reservation."
Acceptance Criteria:
Payment Gateway Integration

✅ The system must support credit/debit cards (Visa, MasterCard) and PayPal.

✅ On successful payment, a booking confirmation email is sent.

Form Validation

✅ If the card number is invalid, display: "Invalid card number. Please check and retry."

✅ If the CVV is missing, show: "CVV is required."

Error Handling

✅ If payment fails (e.g., insufficient funds), allow 3 retries before locking the checkout for 5 minutes.

✅ Display a transaction receipt after success (with booking ID, amount, and date).

Performance

✅ The checkout page must load in <2 seconds (90% of users).

✅ Payment processing should complete within 10 seconds (even during peak traffic).

Security

✅ All card details must be PCI DSS compliant (no raw storage).

✅ Auto-logout after 5 minutes of inactivity during checkout.

User Experience

✅ A progress indicator (Step 1: Booking → Step 2: Payment → Step 3: Confirmation).

✅ Option to save card details (opt-in only).


