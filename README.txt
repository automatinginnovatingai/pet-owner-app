PET OWNER APP – README
======================

Overview
--------
The Pet Owner App is a simple, modern, and secure desktop application designed for everyday
pet owners who want an organized way to track their pets’ health, activities, and care
routines. It centralizes essential information including vaccinations, medications,
appointments, activities, weight history, expenses, and reminders — all in one clean,
easy-to-use interface.

The system is built for clarity, speed, and reliability, with a modular architecture that
supports clean UI separation and a lightweight, scalable local SQL database.

Key Features
------------
• Pet Management
  Create detailed pet profiles with photos, medical notes, weight history, and care details.

• Vaccination Tracking
  Log vaccinations, track due dates, and generate reminders for upcoming shots.

• Medication Tracking
  Record medications, dosage instructions, refill dates, and automated reminders.

• Activities Log
  Track walks, feeding, grooming, training, playtime, and custom activities.

• Appointments
  Manage vet visits, grooming sessions, training appointments, and personal reminders.

• Weight Tracking
  Log weight entries and view progress charts for long-term health monitoring.

• Photo Gallery
  Store and organize pet photos directly inside each pet profile.

• Expenses (Optional)
  Track pet-related expenses such as food, grooming, vet bills, and supplies.

• Reminders & Notifications
  Automated alerts for vaccinations, medications, appointments, and custom tasks.

• Reports
  Generate clean PDF summaries for vet visits, vaccination history, and medication logs.

System Requirements
-------------------
• Windows 10 or later  
• 4–8 GB RAM  
• Local SQL database (SQLite or SQL Server Express depending on build)  
• PDF viewer installed  
• Required Python packages listed in requirements.txt (development mode only)

Installation
------------
1. Install Python 3.10 or later (development mode only).  
2. Install dependencies:  
   pip install -r requirements.txt  
3. Run the database setup:  
   python run_database_setup.py  
4. Launch the application:  
   python main.py  

(End-users installing the packaged `.exe` do not need Python.)

Directory Structure
-------------------
core/
    main.py
    app_controller.py
    router.py

ui_framework/
    ui_main_window.py
    ui_navigation.py
    ui_settings.py

user/
    session_context.py
    centralized_rbac.py (single-role: Owner)

modules/
    pets_ui.py
    vaccinations_ui.py
    medications_ui.py
    activities_ui.py
    appointments_ui.py
    weight_tracker_ui.py
    photo_gallery_ui.py
    expenses_ui.py (optional)
    reminders_ui.py
    reports_ui.py

database/
    db_connection.py
    database_initializer.py
    database_migrations.py

tools/
    validators.py
    formatters.py
    file_manager.py
    pdf_generator.py
    image_processor.py
    export_import.py
    logger.py

assets/
    icons/
    images/
    templates/

docs/
    README.txt
    CHANGELOG.txt
    LICENSE.txt

build/
    requirements.txt
    build_config.json
    app_icon.ico

User Role
---------
Owner  
Full access to all personal pet-care features. No staff, no multi-user roles.

Navigation
----------
Dashboard →  
    My Pets  
        • Pet Profile  
        • Weight Tracking  
        • Photo Gallery  
    Vaccinations  
    Medications  
    Activities  
    Appointments  
    Expenses (optional)  
    Reminders  
    Reports  
    Settings  

Support
-------
automatinginnovatingai@outlook.com

Thank you for using the Pet Owner App!
