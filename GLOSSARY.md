# Overload

A workout tracker for logging training and seeing progress over time, built around progressive overload: gradually doing more weight, reps or volume.

## Language

### Catalogue

**Exercise**:
A specific way of performing a lift or activity, such as Incline Dumbbell Bench Press or Sumo Deadlift. It is what gets logged, and Personal Records and progress are tracked per Exercise.
_Avoid_: Variation, variant

**Retired Exercise**:
An Exercise taken out of the catalogue. It can't be added to new Workouts or Routines, but it stays in history with its Personal Records. Exercises are retired, never deleted.

**Movement**:
A named group of related Exercises, such as Bench Press or Deadlift, used for browsing and search. Each Exercise belongs to exactly one Movement, and the Movement often contains the plain version as its own Exercise (the Pull-up Movement holds Pull-up and Weighted Pull-up).
_Avoid_: Base exercise, exercise family

### Training

**Workout**:
One occasion of training as the user logs it, on a calendar date in the user's time zone with no time of day: an ordered list of Entries. A Workout has no lifecycle; it can be edited at any time, whether it is logged live or afterwards.
_Avoid_: Session, training

**Entry**:
One Exercise's place in a Workout or Routine. In a Workout it holds the Sets done; in a Routine it holds the target number of Sets and a Rep Target.
_Avoid_: Workout exercise, routine exercise, or a bare "exercise" for this

**Set**:
One bout of an Exercise within an Entry, recorded according to that Exercise's Measurement Type. It may be marked as done to Failure and may carry an RPE.

**Set Type**:
Exactly one of warm-up, working or drop. A drop Set follows the Set it drops from, at a lower weight with no rest.

**Superset**:
Two or more consecutive Entries in a Workout or Routine that are done back to back.
_Avoid_: Circuit, giant set

**Measurement Type**:
What every Set of a given Exercise records: weight × reps, reps only, duration, or distance + duration. Each Exercise has exactly one. For weighted bodyweight exercises, the weight is the load added on top of bodyweight.

**RPE**:
Rate of perceived exertion: how hard a Set felt, on a scale of 6 to 10 in half steps.
_Avoid_: RIR

### Progress

**Personal Record**:
The best result a user has achieved on an Exercise in working Sets: for weight × reps, the heaviest weight, the best Estimated One-Rep Max and the best weight at each rep count; for the other Measurement Types, the most reps, the longest duration, the longest distance or the best pace.
_Avoid_: PB, max

**Estimated One-Rep Max**:
The heaviest single rep a Set implies, calculated from its weight and reps with the Epley formula.
_Avoid_: e1RM in user-facing text

**Volume**:
For one Exercise in one Workout, the sum of weight × reps across its working and drop Sets. Only weight × reps Exercises have Volume.

**Streak**:
The number of consecutive weeks, Monday to Sunday in the user's time zone, in which the user met their Weekly Target.

**Weekly Target**:
How many Workouts a user aims to do each week; 3 unless they change it.

### Planning

**Routine**:
A saved, reusable, ordered list of Entries that a Workout can be started from. Starting a Workout copies the Routine, so later edits to the Routine never change past Workouts.
_Avoid_: Template, plan, workout plan

**Rep Target**:
The reps aimed for in every Set of a Routine Entry: a single number, such as 5, or a range, such as 8–12.

**Program**:
A multi-week schedule that says which Routine to do on which day.
_Avoid_: Plan, regimen

### Units

**Preferred Unit**:
The unit (kg or lb, km or mi) a user wants to see values in. A Set keeps the unit it was logged in; values are converted only when comparing across units.
