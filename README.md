Jupyter Notebook: https://github.com/mskeyashah/UCB-ML-Practical-2/blob/main/prompt_II.ipynb

🎯 Objective:
To empower used car dealerships with data-driven insights that enhance pricing strategies and inventory decisions by modeling factors that influence used car prices.

📈 Key Modeling Findings:
We developed and evaluated three regression models — Linear Regression, Lasso Regression, and Ridge Regression — to predict used car prices based on key vehicle features.

✅ Best Performing Model: Ridge Regression
📉 Average Error (MAE): ~$685
📊 Model Reliability: Consistent cross-validation and test set performance indicated strong generalization and no overfitting.
🧰 Preprocessing: Features were scaled and encoded to ensure interpretability and fairness under regularization.
🔍 Business Insights from the Model:
1. Car Age and Condition Matter Most
Car age had a consistent negative impact across all models — older cars are valued lower.
The condition-age interaction term, though small in magnitude, was retained in the best models, suggesting a compounded effect: newer vehicles in better condition yield significantly higher prices.
💡 Strategy: Focus on acquiring newer, well-maintained vehicles, especially those under 5 years old, as they provide the best return potential.

2. Mileage is a Strong Depreciation Signal
The odometer feature was negatively correlated with price across all models.
Even low-age vehicles lose value sharply when mileage exceeds 60,000 miles.
💡 Strategy: Be cautious about stocking high-mileage cars, even if they appear newer.

3. Drivetrain Preferences Influence Value
FWD (Front-Wheel Drive) vehicles had consistently negative coefficients, but were less negative compared to RWD and unknown types.
Indicates a slight preference or better retained value for FWD vehicles, likely due to practicality or regional driving conditions.
💡 Strategy: Prioritize FWD vehicles in regions with wet or snowy climates where they may be more appealing.

4. Fuel Type Patterns Reflect Emerging Trends
All non-gas fuel types (electric, hybrid, other) had negative coefficients, but the magnitudes were relatively similar, suggesting price differences are not extreme — yet.
The Lasso model, when tuned properly, retained EV and hybrid features, indicating their relevance under sparse settings.
💡 Strategy: Closely monitor and adjust pricing strategies for electric and hybrid vehicles, as demand and retained value are likely to increase over time.

5. Brand Matters — Grouped Manufacturer Signals Work Well
Instead of using over 40 individual brands, we grouped them into:

Luxury (e.g., BMW, Mercedes)
Luxury SUV (e.g., Land Rover)
Sports (e.g., Porsche, Ferrari)
Other/common brands (e.g., Toyota, Ford)
The strongest positive coefficient was for manufacturer_sports, showing these cars command substantially higher prices, even after controlling for other features.

💡 Strategy: When possible, invest in sports or luxury vehicles — even with higher mileage or age, they tend to retain higher perceived value.

🧠 Strategic Takeaways for Dealers:
✅ Inventory Priorities: Source newer, lower-mileage vehicles in good condition for optimal resale value.
⚡ EV Opportunity: Stay ahead of electric and hybrid trends. They're gaining traction and may soon hold stronger pricing power.
🚘 Brand Leverage: Recognize the premium associated with sports and luxury brands — these can justify higher pricing and broader marketing appeal.
🌍 Regional Preferences: Consider drivetrain preferences when stocking vehicles. FWD may be favored in certain climates.
