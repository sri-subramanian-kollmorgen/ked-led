# ked-led -- Simulate button press to set fieldbus

## States:
1. Fieldbus Selection-Activation state (entered by long-press >= 10 s). Current fieldbus is displayed (R=EC, G=PN, Y=EIP)
2. Fieldbus Activation state (entered by long-press > 5 and HOLD to select). Each fieldbus color is displayed in slow flash in turn.
3. Fieldbus Selection state (fieldbus selected by releasing button to select). Whichever fieldbus is selected remains solid.

Process of reselecting fieldbus is possible by going to 1. by long-press of 10 s
When finished, power-cycle to enable that fieldbus.
