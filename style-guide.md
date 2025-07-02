# Style guide
This document is intended to synchronise styles across OccamResearchLtd outputs, including both R and Excel models.

## Naming conventions
Variables names should be snake case:

Good:
```
starting_age
```

Bad:
```
startingAge
starting.age
Starting_Age
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
