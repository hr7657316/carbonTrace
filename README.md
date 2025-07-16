# CarbonTrace 🌍

**Carbon Accounting & Reporting Tool for SMEs**

CarbonTrace is an AI-powered carbon footprint tracking and reporting application designed specifically for Small and Medium Enterprises (SMEs). It helps businesses track, analyze, and reduce their carbon emissions across Scope 1, 2, and 3 emissions with intelligent AI assistants.

## 🚀 Features

### Core Functionality
- **Multi-scope Emission Tracking**: Track Scope 1 (direct), Scope 2 (energy), and Scope 3 (value chain) emissions
- **Interactive Dashboard**: Real-time visualization of carbon footprint data with charts and metrics
- **Data Entry & Management**: Manual entry and CSV bulk upload capabilities
- **Multi-language Support**: Available in English and Hindi
- **Enterprise-grade Fields**: Business unit, project tracking, facility management, and verification status

### AI-Powered Insights 🤖
- **Data Entry Assistant**: Get help classifying emissions and mapping to correct scopes
- **Report Summary Generator**: Generate human-readable summaries of emissions data
- **Carbon Offset Advisor**: Personalized recommendations for verified carbon offset options
- **Regulation Radar**: Stay updated on carbon regulations relevant to your business and export markets
- **Emission Optimizer**: AI-powered recommendations to reduce carbon footprint

### Visualizations & Analytics
- Emissions breakdown by scope (pie chart)
- Category-wise emissions analysis (bar chart)
- Time-series emissions tracking (line chart)
- Key performance metrics dashboard

## 🛠️ Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Python 3.8+** - [Download Python](https://python.org/downloads/)
- **Git** - [Download Git](https://git-scm.com/downloads/)
- **GROQ API Key** - Sign up at [GROQ Console](https://console.groq.com/) for AI features

## 📥 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/AIAnytime/Your-Carbon-Footprint.git
cd Your-Carbon-Footprint
```

### 2. Create Virtual Environment

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**On Windows:**
```cmd
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Environment Configuration

Create a `.env` file in the root directory and add your GROQ API key:

```bash
# Create .env file
touch .env

# Add your GROQ API key
echo "GROQ_API_KEY=your_groq_api_key_here" >> .env
```

**To get your GROQ API key:**
1. Visit [GROQ Console](https://console.groq.com/)
2. Sign up or log in to your account
3. Navigate to API Keys section
4. Create a new API key
5. Copy and paste it in your `.env` file

### 5. Create Required Directories

```bash
mkdir -p data
```

## 🚀 Running the Application

### Start the Application

```bash
streamlit run app.py
```

The application will open in your default web browser at `http://localhost:8501`

### Alternative Port (if 8501 is busy)

```bash
streamlit run app.py --server.port 8502
```

## 📖 How to Use CarbonTrace

### 1. First Time Setup

1. **Launch the application** using the command above
2. **Select your language** (English/Hindi) from the sidebar
3. **Navigate using the sidebar menu**:
   - 🤖 **AI Insights** - AI-powered analysis and recommendations
   - 📝 **Data Entry** - Add emission data manually or via CSV
   - 📊 **Dashboard** - View analytics and visualizations
   - ⚙️ **Settings** - Configure company information

### 2. Adding Emission Data

#### Manual Entry:
1. Go to **Data Entry** → **Manual Entry** tab
2. Fill in the emission details:
   - **Basic Info**: Date, business unit, project
   - **Emission Classification**: Scope, category, activity
   - **Location**: Country, facility, responsible person
   - **Measurement**: Quantity, unit, emission factor
   - **Quality**: Data quality and verification status
   - **Notes**: Additional context and sources

#### CSV Upload:
1. Go to **Data Entry** → **CSV Upload** tab
2. Download the sample CSV template
3. Fill in your data following the template format
4. Upload your completed CSV file

**Required CSV Columns:**
- `date`, `scope`, `category`, `activity`, `quantity`, `unit`, `emission_factor`

**Optional CSV Columns:**
- `business_unit`, `project`, `country`, `facility`, `responsible_person`, `data_quality`, `verification_status`, `notes`

### 3. Using AI Features

#### Data Entry Assistant:
- Describe your emission activity in natural language
- Get guidance on proper scope classification and categorization
- Example: "We use diesel generators for backup power at our Mumbai office"

#### Report Summary Generator:
- Automatically generates comprehensive summaries of your emissions data
- Provides insights and key findings in human-readable format

#### Carbon Offset Advisor:
- Get personalized recommendations for verified carbon offset projects
- Based on your total emissions, location, and industry

#### Regulation Radar:
- Stay informed about carbon regulations affecting your business
- Covers local regulations and export market requirements
- Supports EU, Japan, US, China, Indonesia, and India markets

#### Emission Optimizer:
- AI-powered recommendations to reduce your carbon footprint
- Identifies high-impact reduction opportunities
- Provides actionable insights based on your emission patterns

### 4. Dashboard Analytics

The dashboard provides:
- **Total Emissions**: Sum of all recorded emissions
- **Latest Entry**: Most recent data entry date
- **Total Entries**: Count of emission records
- **Scope Breakdown**: Pie chart showing emissions by scope
- **Category Analysis**: Bar chart of emissions by category
- **Time Series**: Line chart showing emissions trends over time

### 5. Data Management

#### Viewing Data:
- All entered data is displayed in a table format on the Data Entry page
- Data is automatically saved to `data/emissions.json`

#### Deleting Entries:
- Use the delete functionality on the Data Entry page
- Select the entry number and click "Delete Selected Entry"

#### Data Backup:
- The application automatically creates backups when saving data
- Backup files are stored in the `data/` directory

## 📁 Project Structure

```
carbonfootprint/
├── app.py                 # Main Streamlit application
├── ai_agents.py          # AI agents for intelligent features
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (create this)
├── data/                 # Data storage directory
│   ├── emissions.json    # Main emissions data file
│   └── emissions_backup.json  # Automatic backup
└── README.md            # This file
```

## 🔧 Dependencies

### Core Libraries:
- **streamlit** - Web application framework
- **pandas** - Data manipulation and analysis
- **plotly** - Interactive visualizations
- **python-dotenv** - Environment variable management

### AI & Machine Learning:
- **crewai** - Multi-agent AI framework
- **crewai_tools** - AI agent tools and utilities
- **langchain_groq** - GROQ language model integration
- **faiss-cpu** - Vector similarity search

### Data Processing:
- **matplotlib** - Additional plotting capabilities
- **seaborn** - Statistical data visualization
- **fpdf** - PDF report generation

## 🌍 Supported Emission Scopes

### Scope 1 (Direct Emissions):
- Stationary Combustion (boilers, furnaces, generators)
- Mobile Combustion (company vehicles, fleet, machinery)
- Fugitive Emissions (refrigerant leaks, SF6 emissions)
- Process Emissions (industrial processes)

### Scope 2 (Indirect Energy Emissions):
- Electricity consumption
- Steam consumption
- Heating and cooling

### Scope 3 (Other Indirect Emissions):
- Purchased goods and services
- Business travel and employee commuting
- Waste generated in operations
- Transportation and distribution
- Use of sold products
- End-of-life treatment
- And 10+ other categories

## 🌐 Multi-language Support

CarbonTrace supports:
- **English** - Full interface in English
- **Hindi** - Complete Hindi translation
- Easy to extend for additional languages

## 🔒 Data Privacy & Security

- All data is stored locally on your machine
- No data is transmitted to external servers (except for AI API calls)
- Automatic backup creation prevents data loss
- Environment variables keep API keys secure

## 🚨 Troubleshooting

### Common Issues:

#### "ModuleNotFoundError" when running the app:
```bash
# Ensure virtual environment is activated
source venv/bin/activate  # macOS/Linux
# or
venv\Scripts\activate     # Windows

# Reinstall dependencies
pip install -r requirements.txt
```

#### "AI features not working":
- Check that your GROQ API key is correctly set in the `.env` file
- Ensure you have internet connectivity for AI API calls
- Verify your GROQ account has sufficient credits

#### "Data not saving":
- Check that the `data/` directory exists and is writable
- Ensure sufficient disk space is available

#### Port already in use:
```bash
# Use a different port
streamlit run app.py --server.port 8502
```

### Getting Help:
- Check the application logs in the terminal for error messages
- Ensure all prerequisites are properly installed
- Verify your `.env` file is correctly configured

## 🤝 Contributing

We welcome contributions! Please feel free to:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📧 Support

For support and questions:
- **Product Owner**: Sonu Kumar
- **Email**: sonu@aianytime.net
- **GitHub**: [AIAnytime/Your-Carbon-Footprint](https://github.com/AIAnytime/Your-Carbon-Footprint)

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [Streamlit](https://streamlit.io/) for the web interface
- AI capabilities powered by [GROQ](https://groq.com/)
- Visualization with [Plotly](https://plotly.com/)
- Multi-agent AI framework by [CrewAI](https://github.com/joaomdmoura/crewAI)

---

**CarbonTrace** - Empowering SMEs to track, analyze, and reduce their carbon footprint with AI assistance. 🌱
