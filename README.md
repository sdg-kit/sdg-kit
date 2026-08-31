# sdg-kit

A kit of research instruments for measuring economic, market, and physical systems, built by one person asking the same question in different domains: can you state a hypothesis before seeing the data, give it a fair chance to fail, and report honestly what happened? Everything here follows that discipline — pre-registered predictions, falsification gates that are allowed to kill the idea, null results published instead of buried, and full provenance for every run.

---

## Published

### MacroDiscovery

**What it does.** Searches a large panel of world economic data — about six million observations covering a thousand indicators across two hundred countries — for candidate relationships between economic quantities: functional forms that fit, network structures that persist, structural breaks that recur. Every candidate is then pushed through a validation gauntlet designed to destroy it: out-of-sample tests, stability checks, and falsification criteria decided before the search runs.

**What it aims to do.** Become a machine for generating economic hypotheses worth a human economist's attention. The long-term goal is question-driven discovery: give it a premise ("does X drive Y in small open economies?") and have it assemble the evidence for and against, ranked by how hard each claim was to kill.

**If it works.** Empirical macroeconomics spends enormous effort manually hunting for relationships one paper at a time. A system that industrializes the *candidate-generation* step — while being more honest than the average paper about what survives scrutiny — changes the economics of doing economics. Even its failures are informative: a relationship that every method refuses to find is evidence too.

### GeoPop

**What it does.** Estimates the population of the world, of every country, and of thousands of individual cities using only satellite data — built-up surface area and nighttime lights — then grades its own answers against UN census-based figures. It runs in two modes: one calibrated on a subset of countries and validated on the held-out rest, and one from first principles with zero census input.

**What it aims to do.** Answer a clean scientific question: how much of demography can you recover from physics alone? Roadmap items include finer spatial resolution and using building *volumes* rather than footprints.

**If it works.** Population data is the denominator of almost every human statistic, yet for much of the world it is stale, modeled, or political. An independent, physics-based estimate — with honest error bars — is a check on official numbers and a fallback where censuses don't reach. The current headline (world population estimated within 8% from orbit) is already a statement about how much cities physically reveal.

---

## In development

### strata

**What it does.** Measures how a cryptocurrency's dependence on Bitcoin is layered across timescales — five-minute, hourly, daily, weekly returns — instead of collapsing it into a single correlation number. The central hypothesis is the *capture clock*: as an asset matures, its coupling to Bitcoin appears first in the slow layers and migrates toward the fast ones, driven by liquidity and arbitrage capacity, and jumping at discrete events like exchange listings and futures launches.

**What it aims to do.** Turn that migration into a measurable, per-asset time constant, and test whether events visibly reset it. The name is the thesis: dependence deposited in layers, read like a geologist reads rock strata.

**If it works.** It would give crypto markets something like a maturity dating method — a way to say *where an asset is in its life cycle* from market data alone. That has direct uses in risk (which assets genuinely diversify and at what horizon), in event studies (did this listing actually integrate the asset?), and as a lens on how market efficiency propagates across timescales in any young asset class.

### implied-states

**What it does.** Recovers what markets believe about the future from two independent sources: the risk-neutral probability distribution implied by option prices, and the real-world probability distribution implied by prediction-market contracts. The ratio of the two is a live measurement of the *pricing kernel* — the premium markets charge for bad states of the world — usually only estimated from decades of history.

**What it aims to do.** Run a "kernel horse race": test whether the prediction-market-based kernel explains and forecasts better than the traditional historical one, through a pre-registered battery of experiments. The deliverable is a public dataset and an academic paper.

**If it works.** The pricing kernel is one of the deepest objects in asset pricing, and measuring it live rather than estimating it from history would be genuinely new. Practically, the gap between what options imply and what prediction markets believe is a real-time gauge of risk premia — useful to researchers, allocators, and anyone who wants to know when markets are paying up for insurance.

### qec

**What it does.** Trains a neural decoder for quantum error-correcting codes built as a hierarchy of small specialists — one tiny network per error-detector, fused by a model that learns, shot by shot, which specialists to trust. It is benchmarked without mercy against the standard decoder (minimum-weight perfect matching) and a literature-standard neural baseline.

**What it aims to do.** Beat the baselines, or fail honestly. The project carries a pre-committed decision gate: if no configuration outperforms the neural baseline, the result stands as a documented negative finding and effort pivots to a different family of codes. As of the last runs, the negative result is winning.

**If it works.** Decoding speed and accuracy are real bottlenecks for fault-tolerant quantum computing, and a decoder built from many cheap specialists could scale where monoliths can't. If it doesn't work, a carefully documented failure of a plausible architecture saves others from re-walking the same path — which is a smaller win, but a real one.

### thermo-solow

**What it does.** Provides the reference implementation for a working paper that adds physics to the standard model of economic growth: production is treated as a physical process that necessarily generates waste, waste damages health, and both feed back into how much an economy can produce. The paper proves that this drag hits long-run output with amplified force, because environmental damage also suppresses capital accumulation. The code implements the model's equations and numerically verifies every proposition in the paper — twenty-one checks, all passing.

**What it aims to do.** Keep theory and code honest with each other, and eventually support the paper's companion work: calibrating the model to real economies and testing whether "thermodynamic drag" explains part of the productivity slowdown observed since the 1970s.

**If it works.** It would give a formal, testable backbone to an intuition many people hold loosely — that dirty growth quietly cannibalizes future output — and a damage-adjusted measure (Thermo-GDP) showing erosion that conventional GDP cannot see. Even as pure theory, it demonstrates a portable standard: a paper whose every claim ships with a script that checks it.

### trailhead

**What it does.** A run-mapping web app in a single HTML file — no build, no server, no accounts. Click out the route you ran, log the effort, pull the actual weather for that time and place. Its party trick: it reads the real street grid around your home and generates runnable routes to a pattern — spirals and snakes that never repeat a block.

**What it aims to do.** It's done. It exists to be used, and to prove that a complete, pleasant tool can fit in one file.

**If it works.** It already does. Its role in this kit is the counterweight: evidence that the person doing the measurement-obsessed research above also ships small, finished, human things.

---

## On the bench

Not yet on GitHub, in various states of undress: a multi-asset crypto direction-prediction research system whose reusable parts — a 474-feature engineering pipeline, exchange data fetchers, leakage audits — are slated for extraction into a clean open toolkit; an evolutionary trading framework where a hundred generated agents compete, breed, and get culled on real outcomes; and the legacy exploratory simulator that thermo-solow's paper grew out of, kept as a historical prototype.
