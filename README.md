# Vending-Machine-with-Verilog
Vending-Machine-with-Verilog

STATE DIAGRAM
<img width="899" height="631" alt="image" src="https://github.com/user-attachments/assets/8c2bea4b-1292-4a8b-a258-4829d92cface" />

GRAPH WITH ADDITION OF 10(2) AND THEN 10(2)
<img width="1575" height="816" alt="image" src="https://github.com/user-attachments/assets/4d794544-10eb-4480-bdb7-c00f226f68fa" />

STATES TRANSITIONS:

PRODUCT COST 15 RUPEES

S0: 0 Rs in Vending Machine
If nothing added: Stay in State 0
OUTPUT = 0, CHANGE = 0

If 5 Rs added: Move to State 1
OUTPUT = 0, CHANGE = 0

If 10 Rs added: Move to State 2
OUTPUT = 0, CHANGE = 0

S1: 5 Rs in Vending Machine
If nothing added:
Incomplete transaction, return the money added as CHANGE (5 Rs), no bottle given.
Move to State 0.
OUTPUT = 0, CHANGE = Rs 5 (01)

If 5 Rs added: Move to State 2
OUTPUT = 0, CHANGE = 0

If 10 Rs added:
Total 15 Rs, dispense a bottle with no CHANGE.
Move to State 0.
OUTPUT = 1, CHANGE = Rs 0

S2: 10 Rs in Vending Machine
If nothing added:
Incomplete transaction, return money added as CHANGE (10 Rs), no bottle given.
Move to State 0.
OUTPUT = 0, CHANGE = Rs 10 (10)

If 5 Rs added:
Complete transaction, dispense a bottle with no CHANGE.
Move to State 0.
OUTPUT = 1, CHANGE = Rs 0

If 10 Rs added:
Customer overpaid; dispense a bottle with CHANGE (5 Rs).
Move to State 0.
OUTPUT = 1, CHANGE = Rs 5 (01)
