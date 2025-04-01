The documents in this folder are described below;-
- The document 'JMRI Configuration dialog part 1.png' shows JMRI's configuration options for the servos.
- The document 'JMRI Configuration dialog part 2.png' shows JMRI's configuration options for the outputs which control frog switching. There are eight outputs, two for each frog.
- The document 'State Machine spreadsheet.png' shows the complete state machine. Any state transitions which are not shown are considered to be invalid.
- The document 'State Machine V2.png' is a simplified graphical version of the complete state machine. For simplicity it does not show movements to position 2.
- Each state transition comprises;-
    - The current state, one of enum State
    - The action which has occurred, one of enum Action
    - An event produced which may be one of;-
        - no event
        - a leaving event
        - a reached event
    - A servo action which may be one of;-
        - no change
        - the servo stops moving
        - the servo starts moving to a new position
    - The new state, one of enum State

