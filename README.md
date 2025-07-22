Ambatovy Hydraulic Power Pack Inspection System
A Streamlit web application for conducting and documenting hydraulic power pack inspections at Ambatovy mining operations.

Features
🏭 Branded Interface: Clean, professional interface with Ambatovy branding
👤 User Management: Technician name and group tracking
📋 Interactive Checklists: Digital forms for inspection items with OK/Not OK options
🌡️ Parameter Monitoring: Temperature and pressure readings with validation
📊 Data Export: Export completed inspections as Word documents or CSV files
🔍 Visual Inspection: Support for both visual and vibration inspections
📱 Responsive Design: Works on desktop and mobile devices
Installation
Local Development
Clone the repository:
bash
git clone <repository-url>
cd ambatovy-inspection-system
Create a virtual environment:
bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:
bash
pip install -r requirements.txt
Run the application:
bash
streamlit run main.py
Open your browser and navigate to http://localhost:8501
Cloud Deployment (Streamlit Cloud)
Push code to GitHub:
bash
git add .
git commit -m "Initial commit"
git push origin main
Deploy on Streamlit Cloud:
Go to share.streamlit.io
Connect your GitHub account
Select your repository
Set the main file path to main.py
Click "Deploy"
Usage
Starting an Inspection
Enter Inspector Information:
Technician Name (e.g., "Rodin")
Group (e.g., "Group A")
Set Inspection Details:
Inspection Date (defaults to today)
Equipment Tag Number
Work Order Number
Select inspection type (Thickener I or II)
Complete Inspection Sections:
Safety: Equipment tags, handrails, housekeeping, terminals
General Rake Condition: Pressures and operating parameters
Reservoir: Oil levels, leaks, contamination, filter status
Hydraulic Drive Unit: Condition, temperatures, bolts
Hydraulic Pump: Pump condition, temperatures, hoses
Data Entry Guidelines
OK/Not OK Items: Use radio buttons to select status
Temperature Readings: Enter numeric values in Celsius
Pressure Readings: Enter values in MPa or kPa as specified
Comments: Add detailed observations in comment fields
Validation: System provides warnings for out-of-range values
Exporting Results
After completing an inspection:

Word Document: Generates a formatted report matching original templates
CSV Export: Creates spreadsheet-compatible data for analysis
File Structure
ambatovy-inspection-system/
├── main.py                 # Main Streamlit application
├── requirements.txt        # Python dependencies
├── README.md              # This documentation
├── .gitignore            # Git ignore file
└── docs/                 # Additional documentation
    ├── original_templates/   # Original Word templates
    └── screenshots/         # Application screenshots
Inspection Sections
1. Safety
Equipment tags status
Handrail and grating condition
Housekeeping and cleaning status
Terminal box and grounding cables
2. General Rake Operating Condition
Drive hydraulic supply oil pressure (MPa)
Rake torque pressure (MPa)
Rake lift pressure (MPa) - Target: 9-10 MPa
3. Reservoir
Oil leak checks
Condensate buildup
Oil contamination assessment
PRV temperatures (1, 2, 3)
Delta pressure across filter (Target: < 300 kPa)
Filter color indicator (Green/Yellow/Red)
4. Hydraulic Drive Unit
General condition and noise assessment
Hold down bolts and foundation
Cooling system integrity
NDE and motor body temperatures
5. Hydraulic Oil Supply Pump
Pump condition and noise
Foundation and mounting
Casing and fitting integrity
Flexible hose condition
Pump temperature monitoring
Technical Specifications
Dependencies
Streamlit: Web framework for the application
pandas: Data manipulation and CSV export
python-docx: Word document generation
datetime: Date and time handling
System Requirements
Python 3.7+
512MB RAM minimum
Web browser with JavaScript enabled
Data Validation
Temperature ranges monitored for normal operating conditions
Pressure readings validated against specifications
Required fields enforced before submission
Customization
Adding New Inspection Items
Create a new function for the section in main.py
Add form elements using Streamlit components
Include the section in the main form
Update export functions to include new data
Modifying Templates
Update the create_docx_report() function to modify Word output
Adjust CSV column structure in export_to_csv() function
Styling
Modify CSS in the st.markdown() sections
Update colors and branding in the style definitions
Troubleshooting
Common Issues
Module Not Found Error:
Ensure all dependencies are installed: pip install -r requirements.txt
Port Already in Use:
Kill existing Streamlit processes or use a different port: streamlit run main.py --server.port 8502
File Export Issues:
Check browser download settings
Ensure sufficient disk space
Getting Help
Check the Streamlit Documentation
Review error messages in the browser console
Verify all required fields are completed
Contributing
Fork the repository
Create a feature branch: git checkout -b feature-name
Commit changes: git commit -am 'Add feature'
Push to branch: git push origin feature-name
Submit a pull request
License
This project is proprietary to Ambatovy and intended for internal use only.

Contact
For support or questions, contact the Ambatovy IT/Engineering team.

Version: 1.0.0
Last Updated: July 2025
Developed for: Ambatovy Mining Operations

