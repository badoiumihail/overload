# Store sets in the unit they were logged in

Each Set stores its weight (or distance) as the value and unit the user entered, for example 45 lb, rather than normalising everything to kg. Each user has a Preferred Unit for display, and values are converted only where Sets in different units must be compared, as in charts and personal records. We chose this over storing canonical kg because converting there and back causes rounding drift (45 lb → 20.41 kg → 44.99 lb), so users would see numbers they never logged.
