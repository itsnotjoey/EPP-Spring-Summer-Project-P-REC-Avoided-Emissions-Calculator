#EPP-P-REC-Calculator

This is a web-based Peace Renewable Energy Credit (P-REC) avoided emissions Calculator.

This calculator estimates the avoided emissions associated with P-REC-backed renewable electricity. It converts a buyer budget into purchasable P-RECs, caps the purchase at annual project supply, and estimates associated avoided emissions under a user-defined baseline mix.

How to use • 1. In Emission_Factors, replace any placeholder emission factors with EPP-approved values. • 2. In Inputs, enter project supply, buyer budget, P-REC price, project emission factor (if any), and the baseline mix shares. • 3. Check the QA flags in Inputs. Baseline shares must sum to 100.0% and any baseline with a non-zero share should have an emission factor. • 4. Review Buyer_View for the budget-to-P-REC result and Developer_View for annual issuance and revenue potential. • 5. Use Sensitivity to test how results move if baseline emission factors or P-REC prices change.

Core formulas • Blended baseline EF (tCO2e/MWh) = Σ (baseline share × emission factor) • Net avoided EF per P-REC = MAX(blended baseline EF − project EF, 0) × delivery ratio × displacement ratio × conservative factor • P-RECs affordable by budget = budget ÷ P-REC price • P-RECs actually purchased = MIN(P-RECs affordable, available annual P-REC supply) • Total avoided emissions = purchased P-RECs × net avoided EF per P-REC

Important methodological note P-RECs are energy attribute certificates representing 1 MWh of renewable electricity, not carbon offsets. Any avoided-emissions estimate should therefore be reported separately, with its baseline assumptions and system boundaries disclosed.

Recommended version 1 scope Use diesel or grid displacement first. Only include kerosene or wood fuel if EPP has a defensible method to convert those displaced services into an electricity-equivalent emission factor per MWh.
