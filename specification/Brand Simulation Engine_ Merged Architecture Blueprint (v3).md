### **Brand Simulation Engine: Merged Architecture Blueprint (v3)**

**1\. High-Level System Flow (The "Hybrid" Strategy)** This merged architecture successfully fulfills the BuildFest "Final Unified Requirement" by strictly utilizing the Vercel ecosystem, while embedding deterministic mathematical modeling, multi-layered simulations, and specialized localized NLP.

**2\. Core Stack & Infrastructure**

* **Frontend & Dashboard:** Next.js 15 (App Router) deployed on Vercel. Utilizes React Server Components (RSC), Tailwind CSS, shadcn/ui, and Recharts to deliver a responsive, 3-minute demo-ready Campaign Wizard and Analytics Dashboard.  
* **Development & Orchestration:** Built using the Cursor IDE and Anthropic's Claude Code CLI. Claude Code is configured to route through the Vercel AI Gateway, providing seamless observability, token tracking, and centralized LLM key management.  
* **Backend Execution & Task Queues:** Vercel Serverless Functions (Python) handle API routing. Because advanced simulations exceed serverless timeouts, heavy processing is decoupled into a background worker queue (e.g., BullMQ or Inngest).  
* **Data Ingestion:** Firecrawl is used to reliably scrape real-time market data, competitor pricing, and campaign contexts.

**3\. Advanced Simulation Core (Macro, Micro, and Optimization)** To provide true prescript analytics, the architecture abandons simple regression in favor of a three-tiered simulation engine, finalized by deterministic explainability.

* **Macro-Simulation (Bayesian Marketing Mix Modeling):** The foundation is a Bayesian MMM (implemented via libraries like PyMC-Marketing). It decomposes total sales into Base Sales (organic momentum) and Incremental Sales (ad-driven lift). **Crucially, this layer explicitly integrates Adstock transformations to simulate delayed consumer memory and Hill Functions to model the S-curves of diminishing returns, ensuring the mathematical "physics" of consumer behavior are accurate.** By using Bayesian inference, the system utilizes "priors" (historical benchmarks) to maintain mathematical stability even when data is sparse or overlapping.  
* **Micro-Simulation (Agent-Based Modeling & Markov Chains):** To model granular audience behaviors, the system uses Agent-Based Modeling (ABM) to simulate fictive consumers interacting and spreading viral word-of-mouth. Simultaneously, Markov Chains model the stochastic "memoryless" journey of these agents across different digital touchpoints, calculating the exact probability of transition from one ad state to a final conversion.  
* **Optimization Engine (Genetic Algorithms):** To prescribe the perfect budget split, the system utilizes Genetic Algorithms (e.g., the NSGA-II algorithm via the Python pymoo framework). It simulates natural selection across thousands of random budget allocations, calculating combinations (crossover) and random shifts (mutations) to output a mathematically verified "Pareto frontier"—the exact set of allocations that maximizes revenue without degrading any individual channel's performance.  
* **Deterministic Explainability (SHAP):** Before the LLM generates any narrative report, the outputs are passed through a SHAP (SHapley Additive exPlanations) Explainer. This guarantees 100% deterministic explainability by calculating the exact mathematical contribution of every feature (budget, audience, platform) to the final prediction.

**4\. Specialized NLP & Retrieval Pipeline (Bangla Localization)** To secure maximum points in the "Bangla \+ localization capability" category, the pipeline integrates highly specialized open-source models tailored for the region.

* **Sentiment & Feature Extraction:** Upgraded to csebuetnlp/banglabert. Unlike standard models, this utilizes the advanced ELECTRA architecture with a Replaced Token Detection objective, making it exceptionally powerful at natively processing "Banglish" and noisy social media sentiment.  
* **Multilingual Embeddings:** BAAI/bge-m3 handles the vector embedding process. It natively supports dense, sparse (keyword), and multi-vector retrieval across 100+ languages, preserving the semantic meaning of code-mixed Bengali and English queries without losing local context.  
* **Retrieval Database (Optimized):** Qdrant is utilized for vector search, while **Neo4j** powers the Graph database for Hybrid GraphRAG. Swapping to Neo4j establishes an industry-standard graph environment that integrates seamlessly with LangChain's LLMGraphTransformer, significantly reducing database friction during rapid development.

**5\. The LLM Layer & "Offline/Rural Fallback" Mode** The generative synthesis layer is built to operate both in the cloud and securely on edge devices for users with intermittent internet access.

* **Cloud Mode:** Utilizes Claude 3.5 Sonnet (or Gemini 1.5 Flash) via the Vercel AI SDK to ingest the SHAP values, the Pareto frontier metrics, and the MMM output, generating the final, human-readable Campaign Report.  
* **Local LLM Profile (Offline Mode):** For the rural/offline fallback mode, the architecture utilizes Google Gemma 4 deployed locally via Ollama.  
* **Execution Profiling:** To ensure rapid UI rendering during local execution, the system implements a "Fast Profile" that explicitly disables the \<|think|\> token in the system prompt, bypassing the model's heavy internal reasoning loop for routine explanations. A "Deep Profile" is reserved strictly for complex scenario ideation.

**6\. Asynchronous Orchestration & Edge Caching (Demo-Optimized)** Because Bayesian MCMC sampling, Agent-Based Modeling, and Genetic Algorithms require heavy, prolonged CPU computation, the Next.js frontend must be architected to prevent user-facing latency.

* **Server-Side Execution & Decoupling:** Next.js 15 React Server Components (RSC) are utilized to keep the client bundle exceptionally lean. Heavy AI simulation triggers are pushed to a background worker queue (e.g., Redis \+ BullMQ) so they do not block the main Vercel HTTP response thread.  
* **Pitch-Perfect Incremental Static Regeneration (ISR):** To ensure the dashboard loads instantly during the live 180-second pitch, the system utilizes Next.js ISR. **Pre-computed "dummy" scenarios, historical Pareto frontiers, and static Recharts are cached directly on Vercel's global Edge Network.** This completely mitigates cold-start risks and worker queue latency for the judges. As background workers finish new Bayesian simulations, background revalidation processes seamlessly update these cached pages without penalizing the user's critical path.

**7\. BuildFest Scoring Alignment**

* **Final Unified Requirement:** 100% compliant (Next.js 15, Vercel, Cursor, Claude Code, LLMs).  
* **Innovation:** Fuses advanced computational methods (Bayesian MMM with Adstock/Hill functions, ABM, Markov Chains, Genetic Algorithms) with modern LLM orchestration and SHAP explainability.  
* **Technical Execution:** Overcomes Vercel Serverless limitations by implementing decoupled background workers and live-demo-optimized ISR edge-caching for heavy ML workloads.  
* **Bangla \+ Localization:** Natively handles Banglish via ELECTRA-based transformer models and bge-m3 embeddings, coupled with an entirely offline-capable LLM fallback for rural connectivity.

