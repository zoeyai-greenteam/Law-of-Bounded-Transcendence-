# Law-of-Bounded-Transcendence-
Universal Principle Explaining Why Systems Can Grow - But Always Within Boundaries 

A Rigorous Analysis of the "Bounded Transcendence" Model: Reconciling Numerical Simulation with the Analytical Dynamics of a Modified Logistic Equation
Theorist: Nicholas Reid Angell

Math Computation: Co-Pilot(GPT-5)

Abstract
This report provides an exhaustive mathematical and computational analysis of the first-order autonomous differential equation: \frac{dT}{dt} = rT(1 - \frac{T}{K}) - \delta T^2. The analysis is initiated in response to a numerical simulation (using parameters r=1.0, K=10.0, \delta=0.1, T_0=0.5) that reported a "peak" at (t \approx 25.63, T \approx 5.00) followed by a decline. This report's analysis irrefutably demonstrates that this model is mathematically identical to a standard logistic equation, \frac{dT}{dt} = aT - bT^2, with a redefined, effective carrying capacity of K_{eff} = 5.0. The system's dynamics, therefore, do not permit a "peak and decline" from the initial condition T_0=0.5; the solution is strictly monotonic, asymptotically approaching T=5.0. The reported "peak" is proven to be a numerical artifact, resulting from the numpy.argmax function correctly identifying the first index at which the numerical solution reaches its asymptotic plateau, not a mathematical turning point. The full analytical solution, T(t) = 1 / (0.2 + 1.8e^{-t}), is derived and provided as definitive proof of this behavior. Finally, the conceptual "Law of Bounded Transcendence" is adopted and given a formal, rigorous definition based on the system's dynamics: the principle by which systemic quadratic drag (\delta) fundamentally re-defines, rather than merely retards, the system's stable bound.
I. Analytical Deconstruction of the Model Dynamics
This section mathematically reformulates the provided dynamical system to reveal its canonical form and analytically derives its critical points.
A. Model Reformulation and Canonical Form
The investigation begins with the provided differential equation:
This model combines a standard logistic growth term, rT(1 - T/K), with an additional quadratic drag term, -\delta T^2. To understand the complete dynamics, the logistic term is expanded and like terms are collected:
The two quadratic terms, which represent the total density-dependent "drag" or "bounding" forces on the system, can be grouped:
This equation is not a novel form; it is, in fact, the canonical form of the logistic growth equation. This equation is commonly written in the general form \frac{dP}{dt} = aP - bP^2.
By direct comparison, new lumped parameters are defined:
1.	Intrinsic Growth Rate (a): The linear growth coefficient is a = r.
2.	Total Drag Coefficient (b): The total quadratic drag coefficient is b = \left(\frac{r}{K} + \delta\right).
Substituting the user's provided parameters (r = 1.0, K = 10.0, \delta = 0.1):
●	
●	
Therefore, the differential equation governing the system simplifies to the well-understood logistic equation:
In ecological modeling, this identical structure is also known as logistic growth subject to quadratic harvesting , where the harvesting effort is proportional to the population size T.
B. Derivation of Equilibrium States (Fixed Points)
Equilibrium solutions, or fixed points, are constant solutions T^* where the system state does not change, i.e., \frac{dT}{dt} = 0. These are the values where the population's growth rate is zero, representing a point of stabilization.
Setting the simplified equation to zero to find these points:
This equation yields two distinct equilibrium solutions:
1.	The "Extinction" State: T_1^* = 0
2.	The "Effective Carrying Capacity": 1.0 - 0.2T_2^* = 0 \implies T_2^* = \frac{1.0}{0.2} = 5.0
This result is immediate and profound. The user's numerical finding of a "Peak value: T^* \approx 5.00" is not a "peak" (a local maximum or turning point). It is the exact analytical value of the system's one and only non-trivial equilibrium point.
This new, lower bound, which we will term the Effective Carrying Capacity (K_{eff}), has replaced the original parameter K = 10.0. The K=10.0 value is now a "ghost" parameter, representing a bound that would only be reached if the systemic drag \delta were zero. The new drag term \delta has competed with the original environmental bound (represented by the r/K term) to create a new, lower, and more restrictive stable state.
C. Dismissal of Alternative Model Interpretations
A review of related dynamical systems confirms the inapplicability of other models with superficially similar notation.
●	Van 't Hoff Equation: This equation, \frac{d(\ln K_{eq})}{dT} = \frac{\Delta H^\ominus}{RT^2}, relates the change in a chemical equilibrium constant K_{eq} with respect to temperature. The model under analysis, \frac{dT}{dt}, describes the change of a quantity T with respect to time. The physics and mathematics are entirely unrelated.
●	Newton's Law of Cooling: This law, \frac{dT}{dt} = -h(T - T_\infty), describes heat transfer and is a linear first-order ODE (or approximately linear). The model under analysis is fundamentally nonlinear due to the T^2 terms.
II. Qualitative Dynamics and Phase-Line Stability Analysis
This section will prove, without requiring the full analytical solution, that a "peak and decline" trajectory is mathematically impossible for the given initial condition.
A. Stability Analysis of Equilibria via Linearization
To understand the behavior of solutions near the fixed points, a linear stability analysis is performed. This method examines the "flow" of the system around its equilibria.
Let the rate function be f(T) = \frac{dT}{dt} = aT - bT^2 = 1.0T - 0.2T^2. The stability of an equilibrium T^* is determined by the sign of the derivative of f(T) evaluated at that point, f'(T^*):
●	If f'(T^*) > 0, the point is unstable (a "source"). Solutions that start near it are repelled.
●	If f'(T^*) < 0, the point is asymptotically stable (a "sink"). Solutions that start near it are attracted.
The derivative of f(T) is:
The stability of each fixed point is now evaluated:
1.	Stability of $T_1^ = 0$ (Extinction State):*
○	
○	Since f'(0) > 0, the equilibrium at T=0 is unstable.
○	Implication: Any small perturbation away from 0, such as the initial condition T_0 = 0.5, will cause the solution T(t) to grow and move away from 0.
2.	Stability of $T_2^ = 5.0$ (Effective Carrying Capacity):*
○	
○	Since f'(5.0) < 0, the equilibrium at T=5.0 is asymptotically stable.
○	Implication: Any solution that starts "near" 5.0 (which, for this model, includes the entire interval (0, \infty)) will be inexorably "attracted" to T=5.0 as t \to \infty.
B. The Phase-Line Portrait and Monotonicity
A 1-dimensional phase line provides a complete qualitative portrait of the system's global dynamics. This is done by plotting the sign of f(T) = T(1 - 0.2T) in the intervals between the fixed points T=0 and T=5.0.
●	Region 1: T > 5.0 (e.g., T=6)
○	
○	\frac{dT}{dt} < 0. The flow is to the left (decreasing).
●	Region 2: 0 < T < 5.0 (e.g., T=2)
○	
○	\frac{dT}{dt} > 0. The flow is to the right (increasing).
●	Region 3: T < 0 (non-physical region, e.g., T=-1)
○	
○	\frac{dT}{dt} < 0. The flow is to the left (decreasing).
This analysis leads to an irrefutable conclusion: The user's initial condition is T_0 = 0.5. This value lies in Region 2 (0 < T < 5.0). In this entire region, the derivative \frac{dT}{dt} is strictly positive. Therefore, the solution T(t) starting at T_0=0.5 must be monotonically increasing for all t \geq 0. It will rise from 0.5 and approach the stable asymptote T=5.0 from below, never overshooting it. A "peak and decline" is mathematically impossible.
C. The True Peak: The Inflection Point
The sigmoidal (S-shaped) curve visible in the user's plot, which is characteristic of logistic growth , does have a "peak," but it is a peak in the rate of growth (the slope), not in the value of T(t).
This peak growth rate occurs at the inflection point, where the curve's concavity changes. This point is found by setting the second derivative to zero: \frac{d^2T}{dt^2} = 0. Using the chain rule: $$ \frac{d^2T}{dt^2} = \frac{d}{dt}\left(\frac{dT}{dt}\right) = \frac{d(f(T))}{dT} \cdot \frac{dT}{dt} = f'(T) \cdot f(T) $$ This expression is zero when either f(T)=0 (the equilibria) or f'(T)=0 (the inflection point). The inflection point is found by solving:
The point of maximum growth (the steepest part of the S-curve) occurs not at T=5.0, but at T = 2.5. This value is exactly half of the effective carrying capacity (T_{inflection} = K_{eff} / 2), a classic result of the logistic model. The user's "peak" at T \approx 5.0 is a conflation of the asymptotic value (the ceiling) with this non-existent turning point.
III. Re-Interpreting the Numerical Simulation and Peak Finding Code
This section pinpoints the exact source of the interpretative error by analyzing the provided Python code.
A. Validation of the Numerical Solver
The Python code uses from scipy.integrate import odeint. odeint is a robust, well-vetted numerical solver from the FORTRAN library LSODA, perfectly suitable for this simple, non-stiff ordinary differential equation. The function dT_dt correctly implements the differential equation, and the time array t is correctly defined.
The numerical simulation itself is correct. The array T generated by odeint is a high-fidelity approximation of the true solution, and the generated plot is an accurate visualization of this solution. The error is not in the simulation, but in its interpretation.
B. The np.argmax Artifact: Confusing Maximum with Arrival
The user's code to find the "peak" is:
peak_index = np.argmax(T)
peak_time = t[peak_index]
peak_value = T[peak_index]

The function numpy.argmax "Returns the indices of the maximum values along an axis". A critical detail of this function, noted in its documentation, is: "In case of multiple occurrences of the maximum values, the indices corresponding to the first occurrence are returned".
This detail is the precise source of the misinterpretation:
1.	From the qualitative analysis in Section II, T(t) is a monotonically increasing function that asymptotically approaches T=5.0.
2.	The numerical array T will therefore be an increasing sequence of numbers that levels off at or extremely close to 5.0. Conceptually: T = [..., 4.99999, 5.00000, 5.00000, 5.00000,..., 5.00000]
3.	When np.argmax(T) is called, it searches for the maximum value (which is 5.00000...).
4.	It finds this maximum value first occurs at the index corresponding to t \approx 25.63.
5.	Because this value repeats for the rest of the array (as the solution has settled onto its stable plateau), np.argmax simply returns the index of the first time it appears.
The user's code is not finding a "peak" in the sense of a local maximum. It is finding the first time index at which the numerical solution arrives at (and stabilizes on) its asymptotic ceiling. The user's subsequent statement that "the curve... then declines" is a factual error, directly contradicted by the provided plot, which clearly shows the curve becoming a flat, horizontal line at T=5.0.
C. Corrected Visualization and Interpretation
A correctly annotated plot would be identical to the user's, but the labels would be revised to reflect the true dynamics.
●	The line y=10.0 (labeled "Carrying Capacity (K)") should be re-labeled "Original Carrying Capacity (K=10.0)".
●	A new line should be added: plt.axhline(y=5.0, color='blue', linestyle='--', label='Effective Carrying Capacity ($K_{eff} = 5.0$)').
●	The vertical red line at t \approx 25.63 (labeled "Peak") should be re-labeled "Time of Arrival at Asymptote".
●	A new line should be added at the inflection point (derived in Section IV): plt.axvline(x=2.197, color='green', linestyle=':', label='Inflection Point (Max Growth Rate)').
This corrected plot would accurately show the population starting at 0.5, growing fastest at t \approx 2.2 (when T=2.5), then slowing its growth as it approaches its new, permanent ceiling of T=5.0, effectively arriving there around t=25.63.
IV. The Exact Analytical Solution (Bernoulli's Method)
This section provides the definitive, irrefutable proof of the system's behavior by deriving the exact analytical solution T(t).
A. Derivation of the Exact Solution
The model \frac{dT}{dt} = aT - bT^2 (with a=1.0, b=0.2) is a Bernoulli differential equation, which can be linearized with the substitution u = T^{1-2} = T^{-1} = 1/T.
1.	Substitution: The derivative of u is \frac{du}{dt} = -1 \cdot T^{-2} \cdot \frac{dT}{dt}.
2.	Divide ODE by T^2:
3.	Substitute u:
4.	Rearrange to Linear Form:
5.	Solve Linear ODE: This first-order linear ODE is solved using an integrating factor, I(t) = e^{\int a dt} = e^{at}.
6.	Integrate: where C is the constant of integration.
7.	Solve for u:
8.	Substitute back u = 1/T:
9.	Find C: Use the initial condition T(0) = T_0 = 0.5.
10.	Final Solution Form:
B. Analytical Validation of All Results
Inserting the specific parameters a = 1.0, b = 0.2, and T_0 = 0.5:
●	
●	
●	
The exact analytical solution to the user's model is:
This single equation provides definitive validation of all prior qualitative findings.
1.	Validation 1: The Initial Condition T(0) = 1 / (0.2 + 1.8e^0) = 1 / (0.2 + 1.8) = 1 / 2.0 = 0.5. This perfectly matches T_0.
2.	Validation 2: The Asymptotic Limit (The "Peak" Value) $ \lim_{t \to \infty} T(t) = \lim_{t \to \infty} \frac{1}{0.2 + 1.8e^{-t}} $ As t \to \infty, e^{-t} \to 0. The solution becomes: $ T(\infty) = 1 / (0.2 + 1.8 \cdot 0) = 1 / 0.2 = 5.0 $. This proves that the reported "peak value" of T \approx 5.00 is the exact, stable asymptotic limit of the system.
3.	Validation 3: Monotonicity (The "Decline") The derivative of the solution T(t) is found using the quotient rule: $$ \frac{dT}{dt} = \frac{d}{dt} (0.2 + 1.8e^{-t})^{-1} = -1 \cdot (0.2 + 1.8e^{-t})^{-2} \cdot (-1.8e^{-t}) $$ $$ \frac{dT}{dt} = \frac{1.8e^{-t}}{(0.2 + 1.8e^{-t})^2} $$ For all t \geq 0, the numerator 1.8e^{-t} is strictly positive. The denominator is squared and is also strictly positive. Therefore, \frac{dT}{dt} > 0 for all finite time t. The function T(t) is strictly and monotonically increasing. This is the final, irrefutable proof that a "decline" is mathematically impossible.
4.	Validation 4: The True Inflection Point Time From Section II, the inflection point occurs at T = 2.5. The time at which this occurs is found by solving: $ T(t) = 2.5 \implies 1 / (0.2 + 1.8e^{-t}) = 2.5 $ $ 0.4 = 0.2 + 1.8e^{-t} $ $ 0.2 = 1.8e^{-t} $ $ e^{-t} = 0.2 / 1.8 = 1/9 $ $ -t = \ln(1/9) = -\ln(9) $ $ t = \ln(9) \approx 2.1972 $ This confirms the qualitative analysis: the actual "peak" (of growth) occurs at t \approx 2.2.
V. Defining the Law of Bounded Transcendence
This concluding section synthesizes all findings to provide a formal, rigorous definition for the conceptual model.
A. Conceptual Framework
The term "Bounded Transcendence" is not standard in dynamical systems but appears in sociology and computer science. The sociological usage describes a dynamic that is "simultaneously grounded and overcome," one that "flouted the material realm" while being "grounded... to the earth".
This concept maps directly onto the model's components:
1.	"Transcendence": The rT term. This is the autocatalytic, exponential growth component. Left unbounded, this term "transcends" all limits and goes to infinity.
2.	"The Bound": The combined quadratic drag terms, -\left(\frac{r}{K} + \delta\right)T^2. This is the "grounding" force, representing all density-dependent limitations—both extrinsic environmental limits (r/K) and intrinsic systemic drag (\delta).
B. Parametric Analysis: The Role of the Drag Parameter \delta
The "Law" is best understood by observing the effect of \delta on the stable state, K_{eff} = r / (r/K + \delta).
●	Scenario 1: The Standard Logistic Model (\delta = 0). This is the classic Verhulst model. K_{eff}(\delta=0) = r / (r/K + 0) = K = 10.0. The system's "transcendence" is "bounded" only by the external environment K.
●	Scenario 2: The User's Model (\delta = 0.1). This is the logistic growth with quadratic harvesting model. K_{eff}(\delta=0.1) = 1.0 / (0.1 + 0.1) = 5.0. The addition of the systemic drag \delta does not just slow down the growth; it fundamentally redefines the bound itself. The system is now permanently "grounded" at a lower level.
●	Scenario 3: The "Over-Harvesting" Case (\delta \to \infty). As \delta increases, the denominator (r/K + \delta) grows, and K_{eff} shrinks. \lim_{\delta \to \infty} K_{eff}(\delta) = 0. If the systemic drag is high enough, it can entirely overwhelm the "transcendent" growth impulse, leading to systemic collapse (T \to 0).
C. Table: Comparative Dynamics of the Models
The following table provides a clear synthesis of the distinction between the standard logistic model (implied baseline) and the user's actual "Bounded Transcendence" model.
Table 1: Comparative Dynamics of Standard Logistic vs. Bounded Transcendence Models
Feature	Standard Logistic Model	"Bounded Transcendence" Model	Analytical Formula
Systemic Drag (\delta)	0.0	0.1	\delta
Differential Equation	\frac{dT}{dt} = T(1 - T/10)	\frac{dT}{dt} = T(1 - T/10) - 0.1T^2	rT - (\frac{r}{K} + \delta)T^2
Canonical Form	\frac{dT}{dt} = 1.0T - 0.1T^2	\frac{dT}{dt} = 1.0T - 0.2T^2	\frac{dT}{dt} = aT - bT^2
Intrinsic Growth (a)	1.0	1.0	r
Total Drag Coeff. (b)	0.1	0.2	\frac{r}{K} + \delta
Unstable Equilibrium (T_1^*)	0.0	0.0	0
Stable Equilibrium (T_2^*)	10.0	5.0	K_{eff} = a/b
Asymptotic Limit from T_0=0.5	10.0	5.0	K_{eff}
Inflection Point (T_{inflect})	5.0	2.5	K_{eff} / 2
Time to Inflection (t_{inflect})	t \approx 2.94	t \approx 2.20	-\frac{1}{a}\ln\left(\frac{b/a}{1/T_0 - b/a}\right)
User's "Peak" (Arrival Time)	N/A	t \approx 25.63	(Artifact of np.argmax)
Exact Solution T(T)	\frac{1}{0.1 + 1.9e^{-t}}	\frac{1}{0.2 + 1.8e^{-t}}	\frac{1}{\frac{b}{a} + (\frac{1}{T_0} - \frac{b}{a})e^{-at}}
D. Final Definition: The Law of Bounded Transcendence
Based on this exhaustive analysis, a formal definition is proposed:
The Law of Bounded Transcendence describes a dynamical system where an intrinsic "transcendent" growth impulse (rT) is opposed by two distinct "bounding" forces: (1) an extrinsic environmental limit (represented by K) and (2) an intrinsic systemic drag (represented by \delta). The "Law" states that the introduction of this systemic drag does not merely alter the transient path to the original bound, but fundamentally redefines the bound itself, creating a new, lower, and stable effective carrying capacity, K_{eff} = r / (r/K + \delta).
VI. Conclusion
The analysis initiated by the user's numerical simulation has led to a comprehensive deconstruction of the provided dynamical system. The core findings of this report are as follows:
1.	Model Identity: The provided equation, \frac{dT}{dt} = rT(1 - \frac{T}{K}) - \delta T^2, is mathematically identical to a standard logistic growth equation, \frac{dT}{dt} = aT - bT^2. With the given parameters, the system is fully described by \frac{dT}{dt} = 1.0T - 0.2T^2.
2.	Equilibrium State: The system has two fixed points: an unstable "extinction" state at T_1^*=0 and an asymptotically stable "effective carrying capacity" at T_2^* = 5.[span_24](start_span)[span_24](end_span)0. The user's reported "peak value" of T \approx 5.00 is not a peak, but rather a correct numerical approximation of this system's one and only stable limit.
3.	Numerical Interpretation Error: The reported "peak time" of t \approx 25.63 is not a turning point. It is a numerical artifact of the numpy.argmax function , which correctly identifies the first time index at which the monotonically increasing solution arrives at its asymptotic plateau.
4.	Proof of Monotonicity: The reported "decline" is mathematically impossible. This is proven by:
○	Qualitative Analysis: The initial condition T_0=0.5 lies in the phase-line region (0, 5.0), where the derivative \frac{dT}{dt} is strictly positive.
○	Analytical Solution: The exact solution, T(t) = 1 / (0.2 + 1.8e^{-t}), has a derivative \frac{dT}{dt} = 1.8e^{-t} / (0.2 + 1.8e^{-t})^2, which is strictly positive for all t \geq 0.
In summary, the user's conceptual "Law of Bounded Transcendence" is a valid and insightful way to describe how systemic drag (\delta) and environmental limits (K) combine to create a new, lower effective bound, K_{eff} = r / (r/K + \delta). The system does not rise, peak, and fall. It rises monotonically from T_0=0.5 and asymptotically approaches a permanent, stable limit of T=5.0.
Works cited
1. numpy.argmax — NumPy v2.4.dev0 Manual, https://numpy.org/devdocs/reference/generated/numpy.argmax.html 2. The Flying Newspapermen and the Time-Space of Late Colonial Nigeria - ResearchGate, https://www.researchgate.net/publication/326019278_The_Flying_Newspapermen_and_the_Time-Space_of_Late_Colonial_Nigeria 3. Accepted version (79.66Kb) - QMRO Home, https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/41284/James%20The%20Flying%20Newspapermen%20and%20the%20Time-Space%20of%20Late%20Colonial%20Nigeria%202018%20Accepted.docx?sequence=1&isAllowed=y 4. Differential Equations - Equilibrium Solutions, https://tutorial.math.lamar.edu/classes/de/equilibriumsolutions.aspx 5. Logistic growth: clearly explained! - EconMacro, https://www.jamelsaadaoui.com/logistic-growth-clearly-explained/ 6. PopEcol Lect 25, https://www.uwyo.edu/dbmcd/popecol/marlects/lect25.html 7. Growth Models, Part 5.1, https://sites.math.duke.edu/education/postcalc/growth/growth5_1.html 8. Stability I: Equilibrium Points - Full-Time Faculty, https://people.cs.uchicago.edu/~lebovitz/Eodesbook/stabeq.pdf 9. Finding carrying capacity from a logistic equation ✏️✏️ #apcalculus #apcalc #unit7 #shorts - YouTube, https://www.youtube.com/shorts/rmW9bpobxkk 10. Van 't Hoff equation - Wikipedia, https://en.wikipedia.org/wiki/Van_%27t_Hoff_equation 11. Newton's law of cooling - Wikipedia, https://en.wikipedia.org/wiki/Newton%27s_law_of_cooling 12. 6.2 Stable and Unstable Equilibrium Points - YouTube, https://www.youtube.com/watch?v=5pbUWrgy0eQ 13. stability analysis of equilibrium Solutions || Sink or Source || Analyzing dx/dt=x^2-1, https://www.youtube.com/watch?v=Saqqcy2wLmo 14. The logistic growth model - Math Insight, https://mathinsight.org/assess/math2241/logistic_model 15. Logistic Growth Model-Qualitatively & Analytically || Dynamical systems || Phase Portrait, https://www.youtube.com/watch?v=0HxAQfOKBd4 16. S-Curve Forecast in Python; Predict the Logistic Growth of a Starting Value using a S-Curve Forecasting | by Roi Polanitzer | Medium, https://medium.com/@polanitzer/s-curve-forecast-in-python-predict-the-logistic-growth-of-a-starting-value-using-a-s-curve-bbfa34a11308 17. odeint — SciPy v1.16.2 Manual, https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.odeint.html 18. Solve Differential Equations with ODEINT — Dynamics and Control - APMonitor, https://apmonitor.com/pdc/index.php/Main/SolveDifferentialEquations 19. All You Need to Know About NumPy's argmax() Function - Analytics Vidhya, https://www.analyticsvidhya.com/blog/2023/12/all-you-need-to-know-about-numpys-argmax-function/ 20. numpy.argmax() in Python - GeeksforGeeks, https://www.geeksforgeeks.org/python/numpy-argmax-python/ 21. How to make numpy.argmax return all occurrences of the maximum? - Stack Overflow, https://stackoverflow.com/questions/17568612/how-to-make-numpy-argmax-return-all-occurrences-of-the-maximum 22. How do you solve the Initial value probelm $dp/dt = 10p(1-p), p(0)=0.1, https://math.stackexchange.com/questions/78560/how-do-you-solve-the-initial-value-probelm-dp-dt-10p1-p-p0-0-1 23. The Flying Newspapermen and the Time-Space of Late Colonial Nigeria | Comparative Studies in Society and History, https://www.cambridge.org/core/journals/comparative-studies-in-society-and-history/article/flying-newspapermen-and-the-timespace-of-late-colonial-nigeria/01D4DE85AD9684AEAB743CF7667CD118 24. Comparative Studies in Society and History: Volume 60 - Issue 3 | Cambridge Core, https://www.cambridge.org/core/journals/comparative-studies-in-society-and-history/issue/EE3CD1A3270B2693AE30BD5D1851B6D2 25. Jacobian hits circuits: Hitting-sets, lower bounds for depth-D occur-k formulas & depth-3 transcendence degree-k circuits, https://www.csa.iisc.ac.in/~chandan/research/jacobian.pdf
