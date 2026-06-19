# Candidate Patch: Chemical Arbitration Layer

Status: candidate_patch / human_note_source / not_canon
Date: 2026-06-19
Source ID: `rtheory-2026-06-19-chemical-arbitration-layer`
Source note: `01_R_THEORY/SOURCES/2026-06-19_chemical_arbitration_layer_source_note.md`
CSP event: pending until CSP write

## Purpose

This patch formalizes a missing distinction in R Theory's existing use of weights.

Earlier R Theory already allowed behavior to emerge from competition between operators under weights, but the symbol `W` was too compressed. It did not clearly separate:

- stable learned structure;
- current runtime weighting;
- error precision;
- learning rate;
- decision-gate threshold;
- Delta-T width;
- energetic cost;
- threat/safety pressure;
- body and chemical state.

The proposed patch adds a **Chemical Arbitration Layer** or, more precisely, a **BioState-driven Arbitration Layer**.

Core claim:

```text
Brain != static predictor.
Brain = predictive control system + dynamic BioState arbitration of value.
```

## Prior Formula

Compact prior form:

```text
A(t) = DG[ R_t, M_t, DeltaT_t, W_t, Ctx_t ]
```

Problem:

```text
W_t
```

can be misread as a single weight object. This makes the brain look too close to an LLM-style static parameter system.

## New Formula

Expanded form:

```text
A(t) = DG[ R_t, M_t, DeltaT_t, W_struct, W_run(t), Body_t, Chem_t, Ctx_t ]
```

Compact form:

```text
A(t) = DG[ R_t, M_t, DeltaT_t, W_struct, Sigma_t ]
```

where:

```text
Sigma_t = { W_run(t), Body_t, Chem_t, Energy_t, Social_t, Threat_t, Safety_t }
```

## Weight Split

The patch introduces a required split:

```text
W_struct   = relatively stable learned structure / synaptic and procedural weight landscape
W_run(t)   = current runtime operator weights after state modulation
eta_state  = state-dependent learning rate
Pi_err(t)  = error precision / sensitivity to mismatch
Tau_DG(t)  = decision-gate threshold
Mu_DG(t)   = decision-gate margin threshold
Lambda_delay(t) = cost of delay
Kappa_energy(t) = cost of energetic expenditure
Rho(t)     = exploration budget
Beta(t)    = exploitation pressure / inverse temperature
```

Canonical distinction:

```text
W_run(t) != W_struct
```

`W_struct` changes mainly through learning and consolidation.  
`W_run(t)` changes whenever organism state changes, even when no structural learning has occurred.

Runtime modulation:

```text
W_run(t) = Gamma(W_struct, M_t, R_t, DeltaT_t, Body_t, Chem_t, Ctx_t)
```

## BioState

The user's initial wording emphasized hormones in blood. The canonical patch broadens this safely:

```text
BioState_t = { Chem_t, Body_t, Energy_t }
```

where:

```text
Chem_t = { N_t, H_t, I_t }
```

and:

```text
N_t = fast neuromodulatory state
H_t = slower endocrine / hormonal state
I_t = immune / inflammatory / metabolic signaling state
```

Body state:

```text
Body_t = {
  interoception_t,
  fatigue_t,
  pain_t,
  hunger_t,
  arousal_t,
  sleep_pressure_t,
  motor_readiness_t
}
```

Canonical rule:

```text
BioState_t is not background context.
BioState_t is an arbitration layer.
```

It changes not only what is selected, but how selection happens.

## Prediction Under State Modulation

Prediction is not neutral with respect to organism state:

```text
y_hat_{t+Delta} = Predict(M_t, R_t, W_run(t), DeltaT_t, Ctx_t)
```

Since:

```text
W_run(t) = Gamma(W_struct, BioState_t, M_t, R_t, DeltaT_t, Ctx_t)
```

then:

```text
y_hat_{t+Delta}
=
Predict(
  M_t,
  R_t,
  Gamma(W_struct, BioState_t, M_t, R_t, DeltaT_t, Ctx_t),
  DeltaT_t,
  Ctx_t
)
```

Implication:

```text
same context + same learned structure != same prediction
```

if BioState changes.

## Prediction Error Under State Modulation

Base mismatch:

```text
epsilon_t = y_t - y_hat_t
```

State-weighted prediction error:

```text
PE_t = Pi_err(BioState_t, R_t, Ctx_t) * epsilon_t
```

The same mismatch can therefore be treated as:

```text
noise
novelty
threat
reward
irrelevance
urgent update
slow update
```

depending on BioState and context.

Model update:

```text
M_{t+1} = M_t + eta_M(BioState_t, R_t) * U_M(PE_t, Ctx_t)
```

Structural weight update:

```text
W_struct(t+1)
=
W_struct(t)
+
eta_W(BioState_t, R_t) * U_W(PE_t, Reward_t, Salience_t)
```

Runtime reweighting:

```text
W_run(t+1)
=
Gamma(W_struct(t+1), M_{t+1}, R_{t+1}, BioState_{t+1}, Ctx_{t+1})
```

Canonical distinction:

```text
W_struct changes by learning.
W_run changes by state even when no structural learning has occurred.
```

## Operator Selection

Let:

```text
L = { L_1, L_2, ..., L_n }
```

Each operator has utility, cost, delay, risk, novelty value, social value, and habit strength.

Candidate operator score:

```text
score_i(t) =
  Beta(t) * [
      U_i(M_t, R_t, Ctx_t)
    - C_i(Body_t, Energy_t)
    - Lambda_delay(t) * Delay_i
    - Pi_risk(BioState_t, M_t) * Risk_i
  ]
  + Rho(t) * Novelty_i
  + Sigma_social(t) * SocialValue_i
  + Alpha_habit(t) * Habit_i
```

Choice distribution:

```text
P(L_i | S_t) = softmax_i(score_i(t))
```

where:

```text
S_t = { M_t, R_t, DeltaT_t, W_struct, W_run(t), BioState_t, Ctx_t }
```

## DG Patch

DG closes by threshold:

```text
max_i P(L_i | S_t) >= Tau_DG(t)
```

or by margin:

```text
P(L_best | S_t) - P(L_second | S_t) >= Mu_DG(t)
```

The thresholds are themselves state-dependent:

```text
Tau_DG(t), Mu_DG(t)
=
Theta(BioState_t, R_t, Threat_t, Energy_t, TimePressure_t)
```

Implication:

```text
stress / threat / fatigue can close DG earlier;
safety / energy / curiosity can keep Delta-T open longer.
```

## Delta-T Patch

Prior reading:

```text
DeltaT = prediction / simulation window
```

Expanded reading:

```text
DeltaT_t = Delta(R_t, M_t, BioState_t, Ctx_t, Threat_t, Energy_t)
```

Delta-T is therefore not just a cognitive ability. It is also a state permission.

Examples:

```text
threat ↑      -> DeltaT narrows toward immediate action
safety ↑      -> DeltaT widens toward exploration/planning
fatigue ↑     -> DeltaT narrows or becomes unstable
curiosity ↑   -> DeltaT branches into counterfactual search
social risk ↑ -> DeltaT includes social consequence simulation
R3 access ↑   -> DeltaT can include model/rule-level futures
```

## Relation to R Levels

### R0

```text
R0: BioState strongly dominates operator weighting.
```

This is not merely irrationality. It is low-latency state-weighted control: fast DG closure, narrow Delta-T, high influence of pain, threat, hunger, arousal, habit, and motor readiness.

### R1

```text
R1: BioState modulates learning from real feedback.
```

The same result does not produce the same update. Salience, reward, threat, fatigue, and body cost change the update strength.

### R2

```text
R2: BioState controls simulation budget and branch depth.
```

R2 can simulate trajectories, but the number of branches, depth of rollout, and acceptable cost of simulation are state-dependent:

```text
B_R2(t) = B_R2(BioState_t, Energy_t, Safety_t)
```

### R3

```text
R3: BioState constrains access to meta-reflection, but can also become an object of reflection.
```

R3 is not outside chemistry. However, R3 can notice the effect of state on choice:

```text
Why am I weighting this this way?
What state is closing DG too early?
Which BioState variable is biasing the current choice?
```

R3 can then change future conditions of choice:

```text
delay decision
change environment
sleep / rest
eat / hydrate
slow breathing
seek social calibration
remove trigger
reframe problem
```

## Freedom Patch

Prior freedom wording:

```text
Freedom is the capacity of R3 to change the rules of its own choice.
```

Expanded wording:

```text
Freedom is not escape from BioState.
Freedom is partial meta-control over future BioState, M, DeltaT, W_run, and DG thresholds.
```

Formal candidate:

```text
Agency_t = capacity(
  R3_t -> modify { M_t, DeltaT_t, W_run(t), BioState_{t+k}, Tau_DG(t+k) }
)
```

## Brain / LLM Boundary

LLM inference usually has:

```text
fixed parameters theta + context + activations + externally supplied sampling parameters
```

Brain choice has:

```text
W_struct + W_run(t) + BioState_t + Body_t + Energy_t + DG thresholds + state-dependent plasticity
```

Therefore:

```text
LLM and brain may converge at predictive sequence processing,
but diverge at endogenous BioState value arbitration.
```

The key distinction is not:

```text
brain predicts, LLM does not
```

but:

```text
brain predicts and chooses from inside a living, chemically modulated value field.
```

## Error Closed by This Patch

Error ID:

```text
R-ERROR-2026-06-19-MONOLITHIC-W
```

Name:

```text
Monolithic W
```

Symptom:

```text
The formula uses W as if all weighting, thresholds, precision, plasticity, and state costs were one object.
```

Correction:

```text
Split W into W_struct, W_run(t), eta_state, Pi_err, Tau_DG, Mu_DG, delay/energy/risk coefficients, and BioState_t.
```

## Route Boundary

This patch touches R Theory and PNA.

Current route decision:

```text
Primary route: 01_R_THEORY/PATCHES
Secondary review route: 05_PNA motivational-field / organism-state bridge
```

Do not yet:

- update `01_R_THEORY/CANON.md`;
- claim external neuroscience verification;
- collapse this layer into generic motivation;
- treat hormones alone as the entire mechanism;
- treat BioState as a deterministic override of R3.

## Review Gates

Before canon movement:

1. Compare with `05_PNA/HYPOTHESES/2026-05-28_motivational_field_r3_bridge.md`.
2. Add external source cards for neuromodulation, hormonal state, interoception, stress/arousal, prediction-error precision, and state-dependent learning.
3. Test whether the split predicts concrete phenomena better than the old monolithic `W` wording.
4. Decide whether Chemical Arbitration is a core R Theory patch, a PNA bridge, or a cross-theory interface.
5. If accepted, prepare compact `CANON.md` wording and version bump candidate.

## Compact Candidate Canon Wording

For later human review only:

```text
Operator weights in R Theory split into structural weights and runtime weights.
Runtime weights, prediction-error precision, learning rates, Delta-T width, and DG thresholds are dynamically modulated by BioState: neuromodulatory, hormonal, interoceptive, energetic, threat/safety, and social-state signals. The brain is therefore not merely a predictive model, but a predictive control system with living-state arbitration of value.
```
