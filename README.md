🏠 California Housing Equity Predictor
An open-source machine learning system to predict California housing prices and combat the state's severe affordability crisis through transparent, equitable, and explainable AI.
🚨 The Business Problem
California's Housing Affordability Crisis
California faces the worst housing affordability crisis in its history. As of 2025, only 15% of California households can afford a median-priced home—down from 56% in 2012. The median home price has reached $905,680, requiring a minimum annual income of $232,400 to qualify for a mortgage .
Key Crisis Metrics:
485,000+ low-income renter households in Los Angeles County alone lack affordable housing 
2.7 million housing unit shortage statewide 
$180,000 in extra lifetime costs for homeowners stuck with high-rate mortgages 
California home prices are 2.5x the national median 
The Critical Gap
Current Automated Valuation Models (AVMs)—like Zillow's Zestimate—operate as proprietary black boxes. These systems:
❌ Lack transparency in pricing decisions
❌ May perpetuate historical biases that undervalue properties in minority and low-income neighborhoods 
❌ Fail to provide actionable insights for policymakers targeting affordable housing development
❌ Offer no "what-if" scenario modeling for housing policy interventions
The Result: Policymakers, affordable housing developers, and first-time buyers lack the transparent, fair, and interpretable tools needed to make informed decisions in a crisis that affects millions of Californians.
💡 Our Solution
We are building an open-source, ethical alternative to black-box real estate valuation systems—specifically designed for California's affordability crisis.
Core Capabilities
Table
Feature	Business Value
Accurate Prediction	<10% MAPE (Mean Absolute Percentage Error), competitive with commercial AVMs
Explainable AI	SHAP values for every prediction—no black boxes
Equity Auditing	Automated bias detection across income, geography, and density dimensions
Affordability Mapping	Identify census block groups with favorable price-to-income ratios for targeted intervention
Policy Simulation	"What-if" analysis for income growth, zoning changes, and subsidy impacts
Target Users
State & Local Policymakers: Target the $2 billion in housing subsidies effectively 
Affordable Housing Developers: Identify optimal sites for the 56,000–840,000 new units needed 
First-Time Homebuyers: Find affordable areas before they're priced out
Community Organizations: Monitor gentrification and displacement risks
Researchers: Study housing market dynamics with transparent, reproducible models
📊 The Dataset
We use the California Housing Dataset (20,640 census block groups, 1990 Census) as our foundation:
Table
Feature	Description	Business Relevance
MedInc	Median income in block group	Primary affordability driver
HouseAge	Median house age	Maintenance cost indicator
AveRooms / AveBedrms	Average rooms/bedrooms	Space and family accommodation
Population / AveOccup	Density metrics	Demand and overcrowding indicators
Latitude / Longitude	Geographic location	Coastal premium, urban access
MedHouseVal	Target: Median house value ($100,000s)	Affordability benchmark
Why This Dataset Matters:
✅ No missing values → Clean foundation for modeling
✅ Strong correlation (0.69) between income and house values 
✅ Geographic coverage of entire state
✅ Historical baseline to measure how affordability has deteriorated since 1990
🎯 Success Metrics
Our project will be successful when we achieve:
Table
Metric	Target	Current Industry Standard
Prediction Accuracy (MAPE)	<10%	8–12% for commercial AVMs 
Model Transparency	100% SHAP explainability	Proprietary/black-box
Fairness Gap	<5% across demographic groups	Often untested 
Affordability Hotspots Identified	50+ block groups	No current systematic tool
Inference Speed	<100ms per prediction	Varies
🏗️ Project Structure
plain
Copy
california-housing-equity/
├── data/               # Raw and processed datasets
├── notebooks/          # EDA, feature engineering, model training
├── src/                
│   ├── data/           # Data loading and validation
│   ├── features/       # Feature engineering pipeline
│   ├── models/         # Training and prediction
│   └── evaluation/     # Fairness auditing and metrics
├── models/             # Serialized model artifacts
├── reports/            # Generated analysis and figures
├── config/             # YAML configuration files
└── tests/              # Unit and integration tests
🚀 Quick Start
bash
Copy
# Clone the repository
git clone https://github.com/yourusername/california-housing-equity.git
cd california-housing-equity

# Install dependencies
pip install -r requirements.txt

# Run full pipeline
make all
⚖️ Ethical Commitment
This project adheres to Principles for Ethical AI in Housing:
Transparency: Every prediction is fully explainable
Fairness: Active bias testing across protected attributes
Privacy: Aggregate census data only—no individual household information
Accountability: Public audit reports with every release
Purpose: Built specifically for affordability crisis intervention, not speculation
📈 Expected Impact
By providing transparent, equitable housing price predictions, this project aims to:
Inform Policy: Help allocate California's $2 billion annual housing budget to areas of greatest need
Guide Development: Identify the optimal locations for affordable housing construction
Empower Buyers: Enable first-time homebuyers to find affordable neighborhoods before displacement
Advance Research: Provide a reproducible benchmark for ethical ML in real estate
🤝 Contributing
We welcome contributions in:
Bias Mitigation: Novel fairness constraints and optimization techniques
Data Integration: 2020 Census updates, zoning data, transit access
Policy Tools: Additional simulation scenarios (rent control, density bonuses, inclusionary zoning)
Documentation: Case studies of real-world impact
See CONTRIBUTING.md for guidelines.
📚 References
California Housing Partnership. (2025). 2025 Affordable Housing Outcomes Report 
CalMatters. (2025). California Housing Affordability Crisis 
Brookings Institution. (2025). Algorithmic Bias in Real Estate 
Teranet & Environics Analytics. (2025). AVM Benchmark Study 
McKinsey & Company. (2016). A Tool Kit to Close California's Housing Gap 
Up for Growth. (2023). California's Housing Shortage Analysis 
