PET OWNER APP – ARCHITECTURE DOCUMENTATION
==========================================

Overview
--------
The Pet Owner App is a modular, lightweight, and secure desktop application designed for
individual pet owners who want to track vaccinations, medications, activities, appointments,
weight history, expenses, and reminders. The architecture follows a clean separation of
concerns:

• UI Layer (Tkinter Frames)
• Manager/Service Layer (Care & Tracking Logic)
• Engine Layer (Scheduling, Calculations, Forecasting)
• Database Layer (Local SQL database + migrations)
• Utilities Layer (PDF, images, file handling, logging)
• Session Layer (local user context only)

This document describes the structure, responsibilities, and interactions of each module.

--------------------------------------------------
1. CORE APPLICATION LAYER
--------------------------------------------------
These files initialize the application, manage routing, and control frame switching.

• main.py  
  Entry point of the application.

• app_controller.py  
  Central controller that manages UI frames and navigation.

• router.py  
  Defines routing rules and maps UI frames to controller actions.

--------------------------------------------------
2. UI FRAMEWORK LAYER
--------------------------------------------------
Reusable UI components and layout helpers.

• ui_main_window.py  
  Main Tkinter window wrapper.

• ui_navigation.py  
  Navigation helpers and shared UI patterns.

• ui_settings.py  
  Application settings UI (local user only).

--------------------------------------------------
3. USER SESSION MANAGEMENT
--------------------------------------------------
Handles local user context and simple permission gating (single role).

• session_context.py  
  Stores session data (active pet, preferences, reminder settings).

• centralized_rbac.py  
  Simplified RBAC with a single role: Owner.

Role:
- Owner (full access to all personal features)

--------------------------------------------------
4. SHARED FEATURE MODULES
--------------------------------------------------
Reusable modules across the entire system.

• pets_ui.py  
  Pet profiles, medical notes, weight history, and photo gallery access.

• vaccinations_ui.py  
  CRUD + due‑date tracking for vaccinations.

• vaccination_schedule_engine.py  
  Calculates next‑due dates and vaccination status.

• vaccinations_manager.py  
  CRUD operations for vaccinations.

• medications_ui.py  
  Medication logs, dosage tracking, and refill reminders.

• activities_ui.py  
  Walks, feeding, grooming, training, playtime, and custom activities.

• appointments_ui.py  
  Vet visits, grooming sessions, training appointments, and reminders.

• weight_tracker_ui.py  
  Weight logs and trend charts.

• photo_gallery_ui.py  
  Local photo storage and gallery viewer.

• expenses_ui.py (optional)  
  Track pet‑related expenses.

• reminders_ui.py  
  Task reminders and notifications.

• reports_ui.py  
  PDF reports for vaccinations, medications, and vet summaries.

--------------------------------------------------
5. PERSONAL CARE ENGINES
--------------------------------------------------
Logic modules that support calculations and forecasting.

• activity_engine.py  
  Summaries, streaks, and activity insights.

• weight_engine.py  
  Weight trend calculations and chart data.

• reminder_engine.py  
  Determines upcoming tasks, overdue items, and daily reminders.

--------------------------------------------------
6. DATABASE LAYER
--------------------------------------------------
Handles all database connectivity and schema management.

• db_connection.py  
  Centralized local SQL database connection handler.

• database_initializer.py  
  Creates initial tables and seeds data.

• database_migrations.py  
  Schema updates and versioning.

Tables include:
- pets  
- vaccinations  
- medications  
- activities  
- appointments  
- weight_history  
- photo_gallery  
- expenses (optional)  
- reminders  

--------------------------------------------------
7. UTILITIES LAYER
--------------------------------------------------
Shared tools used across modules.

• validators.py  
  Input validation helpers.

• formatters.py  
  Date, currency, and text formatting.

• file_manager.py  
  Directory creation, file handling.

• pdf_generator.py  
  PDF creation with text blocks and images.

• image_processor.py  
  Image resizing and optimization.

• export_import.py  
  CSV/JSON import/export utilities.

• logger.py  
  Application logging.

--------------------------------------------------
8. ASSETS
--------------------------------------------------
Static resources used by the UI.

• /assets/icons/*  
• /assets/images/*  
• /assets/templates/*

--------------------------------------------------
9. UI FLOW
--------------------------------------------------
Dashboard →  
    My Pets  
