# Vega-Lite 5 spec examples

This reporsitory contains example specifications for the params proposal. We are trying to unity selections and signals in Vega-Lite. The example files have names ending with `-signals` (using experimental signals syntax), `-selections` (using selections), and `-params` (using proposed syntax). They are in folders for each example.  

## Summary of Changes

* Introduce scalar parameters (similar to Vega signals) to Vega-Lite
* Unify scalar parameters with Vega-Lite selections as parameters (params)
* Top-level parameter definitions

#### Justification

We've been discussing how we can introduce signal-like features in Vega-Lite for parameterization.  

One way would be to simply add signals in Vega-Lite. However, the selection abstraction that we had also overlaps with signal’s event processing functionality. Each selection also produces an underlying signal that can be referred to in expressions (e.g,. in "filter" and in predicate's test property). Adding signals will inevitability introduces two overlapping concepts in Vega-Lite.

Thus, we are instead proposing a unified parameter abstraction that unifies (1) reactive variables for parameterization and (2) the original selection abstraction. 

For examples, see the different folders in this repo. 

### Selection Propagation Mechanism

Unlike the original Vega-Lite selection, parameters can be defined at any specification level including at the top-level. Thus, we need a different mechanism for propagating how event processing applies to views (and subviews).

## Docs

https://docs.google.com/document/d/1udcfHaemCzj_YLeeX5b7qcQtIaZEduA2yEt9Xiv8qNc/edit#

https://docs.google.com/document/d/1sxFjXQnjAjv8A595ZR3PKh-bkAItddXS-4wG2-Cy4_Q/edit?ts=5ed01138#heading=h.w35dwxo17m4p
