# Style guide
This document is intended to synchronise styles across OccamResearchLtd outputs, including both R and Excel models.

## Naming conventions
Variables names should be snake case:

Good:
```
age_start
```

Bad:
```
ageStart
age.start
Age_Start
```

Names should follow the general heuristic `typeofthing_modifier`:

Good:
```
age_start
```

Bad:
```
start_age
```

Hyphens should be collapsed:

Good:

```
nonHDLC
```

Bad:
```
non_HDLC
```

### Probabilities
Probabilities should begin `prob_` (this is to distinguish them from prices in a health economic context).

Good:
```
prob_death
```

Bade:
```
p_death
death_prob
```

### Proportions 
Proportions should begin `prop_`.

Good:
```
prop_male
```

Bad:

```
p_male
male_prop
```
