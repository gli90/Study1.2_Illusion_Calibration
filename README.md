# Illusion Calibration


## Purpose

In this task(b), we estimates each participant’s illusion magnitude (Δ_illusion) using a color matching / nulling procedure.
The task is designed to quantify how much a chromatic surround biases the perceived color of a central patch.
This calibration is critical for the main experiment, where physical color differences and perceptual color differences will be experimentally dissociated.

## Theoretical Background

The study investigates whether subjective confidence can be dissociated from objective accuracy.
To achieve this goal, we first need to measure:

Perceptual discrimination threshold (task a)  
Δ_threshold    
Estimated using a QUEST adaptive staircase procedure.

This task(b)  
Illusion-induced perceptual bias  
Δ_illusion  
Estimated using a color matching procedure.

The main experiment will later combine these measurements to create stimuli in which:   
Physical color difference  
Perceived color difference  
can be manipulated independently.


## Stimulus Design

### Center Colors

The central patches vary along a calibrated blue–purple color axis (D2 axis).  
Color coordinates are represented in CIELAB space:
(L*,a*,b*)  
with:  
L* = 75  
The D2 axis was selected through pilot testing（candidate axis : A-D）because:  
Blue-purple discrimination is sufficiently difficult.
The transition is perceptually smooth.
Large categorical jumps are avoided.


### Surround Colors

Two large chromatic surrounds are presented:

Left surround  
Green-biased  
(-60, 25)

Right surround  
Red-biased  
(60, 25)  

Pilot testing indicated that this red–green surround pair produces the strongest simultaneous color contrast effect among the tested combinations.


## Experimental Procedure

Each trial contains:

### 1. Fixation

A central fixation cross is presented.  
Duration:  
750 ms


### 2. Matching Phase

Two center patches are shown simultaneously.  

Left center:  
Reference patch

Right center:  
Adjustable comparison patch

Participants move the mouse horizontally to adjust the comparison patch along the blue-purple axis.

Goal:  
Make both center patches appear identical.


### 3. Response

Press:

SPACE

to confirm the match.  
Reaction time is recorded.


### 4. Inter-Trial Interval (ISI)

Fixation cross only.

Random duration:

1000–1500 ms

to reduce adaptation and carry-over effects.


## Multi-Anchor Design

Instead of using a single center color, task_b_ver.1.0 samples multiple locations along the blue-purple axis.

Anchors:

Anchor 1 = (4.0, -29.0)  
Anchor 2 = (5.0, -28.0)  
Anchor 3 = (6.0, -27.0)  
Anchor 4 = (7.0, -26.0)  
Anchor 5 = (8.0, -25.0)

This allows estimation of illusion strength across the color continuum rather than at a single color point.


## Trial Structure

Current version(ver.1.2):

5 Anchors x 8 Repetitions = 40 Trials

Trials are randomized.

For each trial:

Anchor is randomly selected from the shuffled list.
Initial comparison position is randomized.

Starting offsets:

-10  
-8  
-6  
-4  
+4  
+6  
+8  
+10

This minimizes anchoring effects.


## Mouse-Controlled Adjustment

The comparison patch is controlled continuously using horizontal mouse movement.

Advantages:

Continuous response space.  
More natural matching behavior.   
Reduced dependence on repeated key presses.  
Higher precision than discrete button adjustment.

A visual slider is displayed at the bottom of the screen:  

Blue -------- ● -------- Purple

The marker reflects the current adjustment position.


## Recorded Variables

For each trial:

participant  
age  
gender  
trial  
anchor_id  
anchor_a  
anchor_b  
start_offset  
final_offset  
illusion  
rt  

Definitions:

final_offset = final matching position chosen by the participant.

illusion = physical compensation required to null the perceived surround-induced color difference.

rt = reaction time in seconds.


## Outcome Measure

Participant-specific illusion magnitude:

Δ_illusion 

computed as:  
Mean(final_offset)  
across trials.

Additional analyses may examine:  
Anchor-specific illusion magnitude.  
Trial-to-trial variability.  
Reaction time distributions.  
Reliability across sessions.  


## Expected Result

If the surround manipulation is effective:

Mean illusion ≠ 0

A non-zero value indicates that participants systematically compensate for a surround-induced perceptual bias.

This value serves as the participant’s illusion calibration parameter for subsequent experiments.



## Future Integration

This task(b) provides:

Δ_illusion  

Task(a) provides:

Δ_threshold 

The main experiment will use these measurements to construct conditions in which:

Physical Difference
≠
Perceived Difference

allowing confidence and accuracy to be experimentally dissociated.


