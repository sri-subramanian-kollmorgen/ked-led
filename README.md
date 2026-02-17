# ked-led -- Simulate button press to set fieldbus

## Example Sequence:
Assume, current fieldbus is EC (displayed using Red), and we want to change to EIP (Yellow)

1. Press button >= 10 seconds till we see rapid flashing light. Release after.
2. Press button for 5 seconds and HOLD. Slow flashing colors should cycle from R->G->Y->R...
3. When Yellow is displayed, Release button. Yellow will become solid
4. Power-cycle drive.

## States:
1. Fieldbus Menu state (entered by long-press >= 10 s). Current fieldbus color is displayed with rapid flash (R=EC, G=PN, Y=EIP)
2. Fieldbus Selection-start state (entered by long-press > 5 and HOLD button). Each fieldbus color is displayed in slow flash in turn.
3. Fieldbus Selection-complete state (fieldbus selected by releasing button). Whichever fieldbus is selected remains solid.

Process of reselecting fieldbus is possible by going to 1. by long-press of 10 s
When finished, power-cycle to enable that fieldbus.

