
## Checklist:
1. Integrate whether the participant solved the word. **(Done)**
2. Integrate what the participant’s guesses were. 
3. Integrate the answers for the post-experiment questionnaire. **(Done)**
4. If on the word for less than a second or so, remove (these are the ones we skipped past) although this will likely have an exception so verify with the Recording sheet. **(Done)**

## Other applications:
1. Predict whether the word was solved correctly (based on the eye-tracking data and possibly other data as well).  **(Done, with bigrams)**
2. Predict which participant (out of the 29) is working on the anagram.  
3. Do KNN classification of the fixations and see how that corresponds to the location of the letters - okay.
4. Use metrics such as: average time between saccade (how slowly does the participant move their eyes around), the proportion of adjacent sequences - as opposed to moving across the screen, the tendency to scan clockwise versus counterclockwise, time spent within letter radius (dwell duration).  **(Done, except last)**


## Things to do:
1. Make a dataframe with 1 row per participant-word. **(Done)**
2. Fix the issue of the 123456 showing up twice, rename the second one.



