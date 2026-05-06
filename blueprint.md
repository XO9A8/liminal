### Phase 1: Data Ingestion & Feature Engineering (The Inputs)
This is the foundational layer where the engine collects and prepares the data. 
*   **Controllable Marketing Data:** Consolidating historical spend, impressions, pricing, and promotional data from CRM, finance systems, and media platforms `[1]`.
*   **Exogenous/External Data:** Ingesting macroeconomic indicators, seasonality, and competitor proxy data (using intelligence tools like Semrush or Similarweb to estimate competitor traffic and market share) `[2]`, `[3]`.
*   **Creative Feature Extraction:** Using AI vision and Natural Language Processing (NLP) to break down the actual ad creatives into quantifiable features, such as visual saliency (what grabs attention) and textual sentiment `[4]`, `[5]`.
*   **Cold-Start Engine:** For new products with no history, implementing "Transfer Learning" or generating synthetic datasets (artificially generated data that mimics real-world shopping patterns) to safely train the model `[6]`, `[7]`.

### Phase 2: Mathematical Data Transformation
Raw spending data must be mathematically transformed before the AI can analyze it, otherwise, the predictions will be entirely inaccurate.
*   **Adstock Transformation:** Algorithms applied to the data to model the "carryover" or delayed memory effect of an advertisement `[8]`.
*   **Saturation (The Hill Function):** Applying the Hill function to capture the exact point of diminishing returns, where incremental increases in media spend yield progressively smaller increments in sales `[9]`, `[10]`.

### Phase 3: The Core Predictive Engine (The Brain)
This is where the actual machine learning and simulation occur, utilizing three distinct models working together:
*   **Bayesian Marketing Mix Modeling (MMM):** The macro-level forecaster. It uses "informative priors" (incorporating strong existing evidence or historical benchmarks) to narrow down the likely ROI ranges and prevent the model from overfitting to noisy data ``.
*   **Markov Chain Modeling:** The micro-level funnel simulator. It maps out the customer journey as a sequence of state transitions to calculate the "removal effect"—quantifying the exact percentage of conversions you would lose if you removed a specific channel `[11]`, `[12]`.
*   **Agent-Based Modeling (ABM):** The audience simulator. It simulates the behavior of fictive, representative consumers to test highly targeted geographic or demographic strategies that traditional MMM cannot handle `[13]`, `[13]`.

### Phase 4: Prescriptive Optimization (The Strategist)
Once the engine knows how the market reacts, it must figure out the best way to spend the budget.
*   **Genetic Algorithms:** Using evolutionary algorithms (often implemented via Python frameworks like *Pymoo*) to test thousands of potential budget combinations `[14]`, `[15]`.
*   **Pareto Optimization:** The genetic algorithm solves for the "Pareto optimal front," finding the absolute best combination of investments where no single channel's performance can be improved without degrading another ``, ``.

### Phase 5: Dynamic Scenario UI (The Output)
The complex math is hidden behind an executive dashboard designed to answer business questions.
*   **"What-If" Dynamic Scenarios:** An interface allowing marketers to simulate budget decisions (e.g., "What if I reduce Google Ads by 20% and reallocate to Meta?") and instantly see the forecasted impact on sales `[16]`.
*   **Marginal Response Curves:** Visualizations that clearly plot out efficiency peaks and show precisely when an investment crosses into wasted capital `[17]`, `[18]`.
*   **Financial Alignment:** Outputting metrics CFOs care about: Incremental Return on Ad Spend (iROAS), Marginal ROI (mROI), and breaking down total sales into "Base" (organic) vs. "Incremental" (marketing-driven) volume `[19]`, ``.

***

**How to use this blueprint:**
Whenever you feel lost in the technical weeds of a specific algorithm during this competition, look back at this blueprint. It tells you exactly where that piece of math fits into the overarching product.
