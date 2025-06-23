# Universal Statistics of Competition in Democratic Elections - Detailed Summary

## Authors
- **Ritam Pal** (Department of Physics, Indian Institute of Science Education and Research, Pune 411008, India)
- **Aanjaneya Kumar** (Santa Fe Institute, 1399 Hyde Park Road, Santa Fe, NM 87501, USA; formerly IISER Pune)
- **M. S. Santhanam** (Department of Physics, Indian Institute of Science Education and Research, Pune 411008, India)

## Abstract Summary
- **Research Problem**: Elections are complex systems with multitude of agent interactions, yet universal macroscopic patterns independent of microscopic details have not been observed across all scales, countries, and elections
- **Proposed Solution**: Parameter-free voting model that analytically shows margin of victory distribution is driven by voter turnout distribution
- **Key Innovation**: Scaled measure depending on margin and turnout leads to robust universality
- **Validation**: Demonstrated using empirical election data from 34 countries, spanning multiple decades and electoral scales
- **Application**: Deviations from model predictions indicate possible electoral malpractices
- **Significance**: Universality is a stylized fact indicating competitive nature of electoral outcomes

## 1. Introduction and Motivation

### 1.1 Theoretical Foundation
- **Statistical Physics Perspective**: Elections as test-bed for statistical physics principles
  - Multitude of complex interactions between microscopic units (voters)
  - Emergent universal behavior at macroscopic level
  - Examples: gas molecules, spins, earthquakes, financial markets
- **Democratic Governance**: Elections as cornerstone of democratic societies
  - Expression of collective will of citizens
  - Large-scale collective decision-making examples
  - Best-documented instances of human collective behavior

### 1.2 Previous Research Limitations
- **Limited Universality**: Studies focused on single countries or similar electoral protocols
- **Distribution Studies**: 
  - Vote share distribution q(σ) for candidate votes
  - Voter turnout distribution g(τ) for participation
- **Reported Issues**:
  - Deviations from claimed universalities due to electoral district size variations
  - Weak party associations affecting patterns
  - Spatial correlations exist but not universal
- **Missing Element**: No robust universal behavior valid across different scales and countries with vastly different electoral protocols

### 1.3 Research Gap
- Despite enormous election data availability and persistent attempts
- **Core Problem**: Lack of universal emergent behavior valid across:
  - Different scales (polling booth to constituency level)
  - Different countries (34 countries from 6 continents)
  - Different election protocols
  - Multiple decades of data

## 2. Methodology and Model Development

### 2.1 Electoral Process Template
- **Basic Structure**: Candidates compete for votes at each electoral unit
- **Voting Mechanism**: Voters cast votes for only one candidate
- **Winner Determination**: Candidate with largest number of votes wins
- **System Examples**:
  - First-past-the-post (India, UK, USA)
  - Instant-run-off final rounds (Australia)
  - Two-round run-offs final rounds (France)

### 2.2 Key Variables and Definitions
- **Electoral Units**: N units (polling booths, precincts, constituencies, counties)
- **Scale Hierarchy**: 
  - Polling booth (smallest scale)
  - Constituency (largest scale, subsumes many polling booths)
- **Variables**:
  - $c_i$: Number of candidates in i-th electoral unit
  - $v_{i,w}$: Votes for winning candidate in i-th unit
  - $v_{i,r}$: Votes for runner-up candidate in i-th unit
  - $n_i$: Size of electorate (registered voters) in i-th unit
  - $T_i$: Turnout (actual voters) in i-th unit
  - $M_i$: Margin of victory = $v_{i,w} - v_{i,r}$

### 2.3 Random Voting Model (RVM) Development

#### 2.3.1 Model Specification
- **Input**: Raw turnouts $T = \{T_1, T_2, ..., T_N\}$
- **Assumption**: Three candidates per electoral unit ($c_i = 3$)
  - Justification: Top two candidates account for 79% of votes (averaged over 34 countries)
  - Top three candidates account for 87% of votes
- **Voting Probability**: $p_{ij} = w_{ij}/\sum_k w_{ik}$
  - $w_{ij} \in [0,1]$ drawn from uniform distribution
  - Provides natural and effective choice for candidate attractiveness

#### 2.3.2 Model Operation
1. **Setup**: $N$ electoral units with $T_i$ voters each
2. **Probability Assignment**: Random weights $w_{ij}$ from uniform distribution
3. **Normalization**: Convert weights to probabilities $p_{ij}$
4. **Voting Simulation**: Each voter independently chooses candidate based on probabilities
5. **Result Calculation**: Determine winner, runner-up, and margin $M_i$
6. **Statistical Analysis**: Compute sample mean $\langle M \rangle = (1/N)\sum M_i$

#### 2.3.3 Model Properties
- **Parameter-free**: No free parameters to tune
- **Data-driven**: Predictions depend exclusively on actual turnout distribution
- **Universal**: Captures disparate decay features across different countries
- **Scalable**: Works across vastly different electoral scales

## 3. Mathematical Framework and Analytical Results

### 3.1 Large Turnout Limit Analysis ($T \gg 1$)
- **Vote Approximation**: $v_j \approx p_j T$ for j-th candidate
- **Margin Expression**: $M \approx (p_{(3)} - p_{(2)}) T$
  - $p_{(k)}$: k-th order statistics of probabilities
- **Specific Margin**: $\mu = M/T \approx p_{(3)} - p_{(2)}$
- **Key Insight**: $\mu$ distribution has no explicit dependence on $T$

### 3.2 Analytical Distribution Derivation
- **Joint PDF**: $P(w_{(1)}, w_{(2)}, w_{(3)}) = 6$ for $0 < w_{(1)} < w_{(2)} < w_{(3)} < 1$
- **Specific Margin Distribution**:
  $$P(\mu) = \frac{(1 - \mu)(5 + 7\mu)}{(1 + \mu)^2(1 + 2\mu)^2}$$
- **Mean Value**: $\langle\mu\rangle = \frac{1}{2} + \ln\left(\frac{9\sqrt[4]{3}}{16}\right)$
- **Scaled Distribution**: $F(x) = \langle\mu\rangle P(x\langle\mu\rangle)$ where $x = \mu/\langle\mu\rangle$

### 3.3 Universal Scaling Function
- **Key Result**: $F(x)$ is universal and independent of turnout distribution $g(T)$
- **Validation**: Simulations with power law, Gaussian, and uniform $g(T)$ distributions
- **Agreement**: Simulated distributions collapse on analytical prediction
- **Empirical Confirmation**: 32 countries show excellent agreement with universal curve

## 4. Empirical Validation and Results

### 4.1 Figure 1: Turnout and Scaled Margin Distributions
- **Countries Analyzed**: India, USA, South Korea, Canada, Japan, Germany
- **Panel (a)**: Turnout distribution $g(T)$ for different countries
  - **Caption Summary**: Shows striking differences in shapes and ranges for $g(T)$ across countries
  - Germany: Unimodal character
  - Canada & USA: Multiple peaks
  - Clear dissimilarities in shape and support across countries
- **Panels (b-g)**: Scaled margin distribution $f(M/\langle M \rangle)$ for each country
  - **Caption Summary**: Empirical data (open circles) and model predictions (solid lines) show excellent agreement
  - RVM predictions capture disparate decay features
  - Lighter shade shows variability from multiple RVM realizations
  - Germany: Sharp cutoff pattern
  - India & Japan: Slower decay patterns

### 4.2 Figure 2: Scale Independence Validation
- **Countries**: India, USA, Canada at two different scales
- **Panel (a)**: Turnout distributions $g(T)$ at two scales
  - **Caption Summary**: Dashed lines for smaller scales (polling booth/county), solid lines for larger scales (constituency/congressional district)
  - Striking differences in range and shape of $g(T)$ across scales
- **Panels (b-g)**: Scaled margin distributions $f(M/\langle M \rangle)$
  - **Caption Summary**: Empirical data (open circles) and RVM predictions (lines) show excellent agreement despite scale differences
  - **Scale Comparison**:
    - **India**: Polling booths (~10³) vs Parliamentary constituencies (~10⁶)
    - **USA**: Counties vs Congressional districts  
    - **Canada**: Polling booths vs Constituencies
  - Same RVM without parameter adjustments works at both scales
  - Lighter shade represents variability from multiple RVM realizations

### 4.3 Figure 3: Universal Distribution Demonstration
- **Panel (a)**: RVM predictions for different turnout distributions
  - **Caption Summary**: $F(x)$ predicted by RVM for three different $g(T)$ (inset)
  - Open circles from RVM simulations with $N=10^6$
  - Solid colored circles from RVM with empirical $N$ values
  - Red line shows analytical $F(x)$ from Equation
  - Perfect collapse on analytical prediction despite different $g(T)$
  - **Panel (b)**: Empirical validation across 32 countries
    - **Caption Summary**: Empirical distribution of $x=\mu/\langle\mu\rangle$ from 32 countries (excluding Ethiopia and Belarus)
  - Each color represents specific country with consolidated election data
  - Average empirical distributions (red circles) follow analytical curve (red line)
  - Black circles show averaged RVM predictions
  - Inset shows distributions on linear scale

### 4.4 Figure 4: Electoral Fraud Detection
- **Caption Summary**: Distributions $f(M/\langle M \rangle)$ and $F(x)$ from Belarus (2004-2019) and Ethiopia (2010) show significant deviations from model predictions
- **Panel (a)**: Scaled margin distribution $f(M/\langle M \rangle)$
  - Significant deviation from RVM predictions (red line)
  - Light red shaded region shows variability in RVM prediction
- **Panel (b)**: Scaled specific margin distribution $F(x)$
  - Pronounced deviations from universality
  - Statistical evidence of electoral irregularities
- **Validation**: Independent investigations confirm electoral issues in both countries
- **Application**: RVM provides effective statistical toolbox for fraud detection

## 5. Supplementary Material Analysis

### 5.1 Mathematical Derivations (Sections S1-S3)

#### 5.1.1 Specific Margin Distribution Calculation
- **Order Statistics Framework**: Using joint probability distribution of $w_{(1)}, w_{(2)}, w_{(3)}$
- **Delta Function Integration**: 
  $$P(\mu) = 6\iiint \delta\left(\mu - \frac{w_{(3)} - w_{(2)}}{w_{(1)} + w_{(2)} + w_{(3)}}\right) dw_1dw_2dw_3$$
- **Final Result**: 
  $$P(\mu) = \frac{(1 - \mu)(5 + 7\mu)}{(1 + \mu)^2(1 + 2\mu)^2}$$

#### 5.1.2 Margin Distribution for Different Turnout Distributions
1. **Exponential**: $g(T) = (1/\tau)e^{-T/\tau}$
   - Large margin limit: $Q(M) = (\tau/3M^2)e^{-M/\tau}$
   - Same exponential decay rate as turnout

2. **Power Law**: $g(T) = (\alpha-1)T_{\min}^{1-\alpha} T^{-\alpha}$
   - For $M > T_{\min}$: $Q(M) \propto M^{-\alpha}$
   - Same power law exponent as turnout

3. **Gaussian**: $g(T) = C_0e^{-(T/T_0)^2}$
   - Large margin limit: $Q(M) = (C_0/12)(T_0/M)^4e^{-(M/T_0)^2}$
   - Gaussian decay similar to turnout

4. **Uniform**: $g(T) = 1/(b-a)$ for $T \in [a,b]$
   - Sharp cutoff corresponding to finite support

### 5.2 RVM Simulations with Synthetic Data (Section S4)
- **Figure S1**: Margin vs turnout distribution correlations
  - **Caption Summary**: Margin distribution $Q(M)$ plotted with turnout distribution $g(T)$ demonstrating tail correlation
  - Panels (a)-(d): Gaussian, exponential, power law, uniform turnout distributions
  - Blue circles: turnout distributions
  - Red circles: margin distributions from RVM simulations  
  - Black lines: analytical predictions using Equation from Section S3
  - Excellent agreement between analytical and simulation results
  - Panels (e)-(f): USA county-level and congressional district-level validation

### 5.3 Sensitivity Analysis (Section S5)
- **Figure S3**: Different probability assignment protocols
  - **Caption Summary**: Prediction of scaled margin distribution for three different protocols of choosing $p_i$
  - Protocol 1: Standard uniform random weights
  - Protocol 2: Sequential uniform assignment
  - Protocol 3: Equal probabilities (1/3 each)
  - Panels (a)-(c): uniform, Gaussian, power law turnout distributions
  - Model predictions robust for protocols 1 and 2, protocol 3 produces different results

### 5.4 Comprehensive Country Analysis (Section S7)
- **Figure S4**: Scaled margin distributions for all 32 countries
  - **Caption Summary**: Empirical distribution of scaled margins (colored circles) with RVM predictions (black solid lines)
  - Each country shown with empirical data
  - Excellent agreement across diverse electoral systems
- **Figure S5**: Scaled specific margin distributions for all 32 countries
  - **Caption Summary**: Empirical distribution of scaled specific margin (colored circles) with RVM predictions (black solid line)
  - Universal behavior demonstrated across all countries
  - Individual country fluctuations around universal curve

## 6. Data Collection and Processing

### 6.1 Data Sources
- **CLEA Database**: Constituency-Level Election Archive for 180 countries
- **National Sources**: 
  - India: Election Commission website
  - Canada: Election Commission website  
  - USA: MIT Election Data + Science Lab
- **Data Formats**: Tabular to machine-generated and scanned PDFs

### 6.2 Data Cleaning and Validation
- **Quality Control**: 
  - Minimum 400 data points per country
  - Exclude zero turnout cases
  - Require at least two candidates
  - Sum of valid votes = turnout for consistency
- **Final Dataset**: 34 out of 180 countries meet criteria
- **Statistical Robustness**: Threshold ensures universality demonstration and fraud detection capability

### 6.3 Country Summary Statistics (Table S1)
**Representative Examples**:
- **India**: 18 elections (1951-2019), 8,389 constituencies, mean turnout 5.69×10⁵, mean margin 8.33×10⁴
- **USA Congressional**: 167 elections (1788-2020), 33,946 districts, mean turnout 1.14×10⁵, mean margin 2.96×10⁴
- **Canada Polling Booths**: 7 elections (2004-2021), 489,919 booths, mean turnout 5.56×10², mean margin 1.35×10²

## 7. Key Contributions and Implications

### 7.1 Theoretical Contributions
1. **Universal Scaling Discovery**: First demonstration of robust universality in electoral statistics
2. **Turnout-Margin Relationship**: Analytical proof that turnout distribution drives margin distribution
3. **Parameter-Free Modeling**: RVM requires only turnout data as input
4. **Scale Independence**: Universal behavior across 3+ orders of magnitude in electoral unit size

### 7.2 Methodological Innovations
1. **Order Statistics Application**: Novel use of order statistics for electoral analysis
2. **Specific Margin Concept**: $\mu = M/T$ as turnout-independent competitiveness measure  
3. **Multi-Scale Validation**: Systematic analysis across different electoral scales
4. **Cross-National Validation**: 34 countries across 6 continents

### 7.3 Practical Applications
1. **Electoral Integrity**: Statistical fraud detection tool
2. **Comparative Analysis**: Framework for comparing electoral systems
3. **Prediction Capability**: Forecasting margin distributions from turnout alone
4. **Policy Implications**: Understanding competitiveness in democratic elections

### 7.4 Stylized Facts Established
1. **Universality in $F(x)$**: Scaled specific margin distribution is universal
2. **Turnout Drives Margins**: $g(T)$ determines $f(M/\langle M \rangle)$
3. **Scale Invariance**: Results hold across vastly different electoral scales
4. **Cross-National Validity**: Universal patterns transcend national boundaries

## 8. Significance and Future Directions

### 8.1 Scientific Impact
- **Complex Systems**: New example of emergent universal behavior
- **Statistical Physics**: Application to social systems with predictive power
- **Political Science**: Quantitative framework for electoral analysis
- **Applied Mathematics**: Order statistics in real-world complex systems

### 8.2 Democratic Governance Implications
- **Election Monitoring**: Statistical tools for detecting irregularities
- **System Design**: Understanding factors affecting electoral competitiveness
- **International Comparison**: Objective metrics for democratic health
- **Early Warning**: Identifying potential electoral problems

### 8.3 Future Research Directions
1. **Extension to Other Electoral Systems**: Proportional representation, ranked choice
2. **Temporal Dynamics**: Evolution of universality over time
3. **Causal Mechanisms**: Understanding why universality emerges
4. **Refinement of Fraud Detection**: Improving sensitivity and specificity

## 9. Conclusions

This groundbreaking work establishes the first robust universal behavior in electoral statistics, demonstrating that:

1. **Voter turnout distributions contain fundamental information** about electoral competitiveness encoded in margin distributions
2. **Universal scaling emerges naturally** from the basic mechanics of competitive elections, independent of specific electoral protocols or national contexts
3. **Statistical physics principles apply powerfully** to democratic processes, revealing hidden order in apparently chaotic electoral outcomes  
4. **Practical tools for election monitoring** can be developed from theoretical understanding of electoral universality
5. **Democratic health can be quantitatively assessed** using deviations from universal scaling patterns

The work represents a paradigm shift from studying elections as unpredictable political phenomena to understanding them as complex systems with discoverable universal laws, opening new avenues for both theoretical research and practical applications in safeguarding democratic integrity worldwide. 