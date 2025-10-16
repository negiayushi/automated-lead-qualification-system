Automated Lead Qualification System
An intelligent system for automatically qualifying and scoring sales leads based on multiple criteria.
Features

Automated Lead Scoring: Scores leads based on budget, timeline, company size, decision-maker status, and engagement level
Lead Categorization: Automatically categorizes leads as Hot, Warm, or Cold
Data Management: Store and retrieve lead information efficiently
Report Generation: Generate detailed reports and analytics
CSV Export: Export lead data for external analysis

Scoring Criteria
CriterionHighMediumLowBudget30 pts20 pts10 ptsTimeline25 pts (immediate)15 pts (short)5 pts (long)Company Size20 pts (enterprise)15 pts (medium)10 pts (small)Decision Maker15 pts (yes)-5 pts (no)Engagement10 pts (high)5 pts (medium)0 pts (low)
Lead Categories:

Hot (≥70 points): High priority, ready for immediate follow-up
Warm (40-69 points): Medium priority, nurture and engage
Cold (<40 points): Low priority, long-term nurturing

Installation

Clone the repository:

bashgit clone https://github.com/yourusername/lead-qualification-system.git
cd lead-qualification-system

Create a virtual environment (recommended):

bashpython -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install dependencies:

bashpip install -r requirements.txt
Usage
Run the application:
bashpython main.py
Menu Options:

Add New Lead: Manually input lead information
View All Leads: Display all stored leads
View Leads by Category: Filter leads by Hot/Warm/Cold
Generate Report: View detailed analytics and top leads
Export to CSV: Export lead data to CSV file
Load Sample Data: Load test data for demonstration

Project Structure
lead-qualification-system/
├── src/
│   ├── lead_scorer.py      # Lead scoring logic
│   ├── data_handler.py     # Data storage and retrieval
│   └── report_generator.py # Report generation
├── data/
│   └── leads.json          # Lead database
├── main.py                 # Main application
├── requirements.txt        # Dependencies
└── README.md              # Documentation
Example Usage
pythonfrom src.lead_scorer import LeadScorer
from src.data_handler import DataHandler

# Initialize
scorer = LeadScorer()
handler = DataHandler()

# Add and qualify a lead
lead = {
    'name': 'John Doe',
    'email': 'john@example.com',
    'company': 'Example Corp',
    'budget': 'high',
    'timeline': 'immediate',
    'company_size': 'enterprise',
    'decision_maker': 'yes',
    'engagement': 'high'
}

qualified_lead = scorer.qualify_lead(lead)
handler.add_lead(qualified_lead)
Future Enhancements

Email integration for automated follow-ups
Machine learning-based scoring
CRM integration
Web-based dashboard
API endpoints
