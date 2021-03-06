##Description:

A Pseudo-Random Number Generator (PRNG) is initialized from a predictable seed, such as the process ID or system time.

The use of predictable seeds significantly reduces the number of possible seeds that an attacker would need to test in order to predict which random numbers will be generated by the PRNG.

##Mitigation:


PHASE

DESCRIPTION:Use non-predictable inputs for seed generation.

PHASE:Architecture and Design Requirements:STRATEGY:Libraries or Frameworks:
Use products or modules that conform to FIPS 140-2 [REF-267] to avoid obvious entropy problems. Consult FIPS 140-2 Annex C (Approved Random Number Generators).

PHASE:Implementation:
Use a PRNG that periodically re-seeds itself using input from high-quality sources, such as hardware devices with high entropy. However, do not re-seed too frequently, or else the entropy source might block.

